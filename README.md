# Braintree Flask Example
[![Build Status](https://travis-ci.org/braintree/braintree_flask_example.svg?branch=master)](https://travis-ci.org/braintree/braintree_flask_example)

An example Braintree integration for python in the Flask framework.

## Setup Instructions

1. Install requirements:
  ```sh
  pip install -r requirements.txt
  # or
  docker-compose build
  ```

2. Copy the contents of `example.env` into a new file named `.env` and fill in your Braintree API credentials. Credentials can be found by navigating to Account > My User > View Authorizations in the Braintree Control Panel. Full instructions can be [found on our support site](https://articles.braintreepayments.com/control-panel/important-gateway-credentials#api-credentials).

3. Start server:
  ```sh
  python app.py
  # or
  docker-compose up
  ```

  By default, this runs the app on port `4567`. You can configure the port by setting the environmental variable `PORT`.

## Running tests

Unit tests do not make API calls to Braintree and do not require Braintree credentials. You can run this project's unit tests by calling `python test_app.py` on the command line.

## Testing Transactions

Sandbox transactions must be made with [sample credit card numbers](https://developers.braintreepayments.com/reference/general/testing/python#credit-card-numbers), and the response of a `Transaction.sale()` call is dependent on the [amount of the transaction](https://developers.braintreepayments.com/reference/general/testing/python#test-amounts).

## Notes

You can test a transaction with amount : 0.01€ and credit card 5555555555554444.
