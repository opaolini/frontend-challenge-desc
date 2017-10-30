# Intro
Welcome to the Frontend Challenge!
   
The premise is simple, you have to create a "blockchain address explorer" using https://blockchain.info/api/blockchain_api

The goal of this is to create a single page app that will showcase some of your frontend development skills.

You can draw the inspiration from https://blockchain.info itself, it will also help you gain better understanding of the API and underlying relations.

## Specification and Wireframes

The API call that you will need to complete this task is: https://blockchain.info/rawaddr/$bitcoin_address 

To test an address with plenty of transactions you can for example use this address: `1F1tAaz5x1HUXrCNLbtMDqcw6o5GNn4xqX` (quite famous - contains the Silk Road funds)

The app itself is quite simple and consists of two views.

### Landing - root path
![Landing](/images/landing.png)


* Contains title / fake logo and some space for additional information
* Has a text input which will be used by to user to type in the bitcoin address.
* The text input itself should be `in focus` whenever the user lands on this page allowing for instant input.
* On invoking the search action user should be taken to the next view.
* (OPTIONAL) - Maybe some input validation if you feel like it. A simple validation would check if the first value is either a `1` or `3` a more advanced one would use a proper Bitcoin address validation. Hint - there are libraries for that ;)


### Address detail view - /address/<addr>
![Details](/images/detail.png)


* Shows address in the top part of the view.
* Shows the stats regarding the address: `total_received`, `total_sent`, `final_balance` . (OPTIONAL) Format these values.
* Contains a table of transactions - they are included in the response object from the API
* The transaction row should contain: the date (parsed from timestamp into human readable form), amount, and the address it was sent to.
* The `receiver_address` in transaction row should be CLICKABLE and should be redirect users to `/address/receiver_address`

## Key Requirements

* This should be a Single Page App.
* Use either `npm` or `yarn`
* Use the reactive framework of your choice.
* It should include a router to easily navigate back and forward.
* It should contain at least one unit test invoked with `npm test`.
* When you will be finished with the development, please upload it to a public GitHub repo and send over an email with the link :)
* Running as a dev should work out of the box with `git clone` -> `npm install` -> `npm start`
