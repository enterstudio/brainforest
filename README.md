# brainforest

[Braintree](https://www.braintreepayments.com/) provides a suite of tools to enable easy payment processing in an application, including a drop-in UI that validates credit card info and integrates with PayPal.  The simplest version of that UI uses query selectors to insert a pre-built form into the DOM.  If your view code is already manipulating the DOM imperatively, the drop-in UI is a great git, but if your application is built with React, using the drop-in UI means losing the power of describing UI as a function of data.

Other projects have already implemented [React wrappers around the drop-in UI](https://github.com/jeffcarp/braintree-react), but that doesn't really address the core paradigm discrepancy.  

This project is (currently) a reference implementation for adding Braintree to a React/Redux app, and aims to eventually be a set of higher order components you can use that take advantage of React's component lifecycle hooks and declarative syntax.

## overview

**brainforest** is essentially a [direct tokenization implementation](https://developers.braintreepayments.com/reference/client-reference/javascript/v2/credit-cards#credit-card-direct-tokenization) of Braintree's client API, powered by a Node server that connects to Braintree's server API.  It uses some of Braintree's other open source projects, specifically [card-validator](https://github.com/braintree/card-validator), to handle (you guessed it) credit card validation.

### Features
- Live validation
- Dynamic input formatting
- Credit card validation with card type logos

## Usage

_To run the demo locally:_

```
git clone https://github.com/ellismarkf/brainforest.git
cd brainforest
npm install
npm run start:dev
```
Then visit `http://localhost:3000` in your browser.

_To use **brainforest** in your project:_

Study (copy) the source code and implement (paste) as necessary.  It's my goal to eventually publish this as an npm module, such that it can be imported into a project and "Just Work", but it's not at that stage yet.