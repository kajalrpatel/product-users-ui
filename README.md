# React Redux Address Book

## Introduction

Address Book app enables Users to search for Contact Details of their friends, family, etc. The app is 99% ready, but there are some bugs and pieces of code missing. Fix them!

project uses **React Hooks**, **Redux** and **React Testing Library (`@testing-library/react`)**.

## Data sources

1. The app is communicating with an asynchronous fake HTTP API implemented in `src/httpApi/fakeHttpApi.js`.

2. Mock data is used. There are 1000 fake contacts defined in . In `src/httpApi/contacts.json`.

### App specifications

**Searching:**

* User can type text in `<PhraseInput>`.

* HTTP request asking for top 5 matching contacts is made for every update in the search phrase typed by User, but…

* Whenever matching contacts are fetched, `<MatchingContacts>` appears populated with contacts.

* If any error happens during search request (such as making requests too fast), `<SearchFailure>` appears below `<PhraseInput>`. 
`<SearchFailure>` disappears when the new text is typed in `<PhraseInput>`.
  
* User can select a contact from matching contacts by pressing enter or clicking a mouse while navigating either up or down from `<PhraseInput>` into `<MatchingContacts>`.

* Whenever User selects one of the matching contacts, the search phrase is replaced with text (name) of chosen contact.

**Contact Details:**

* When User selects a matching contact, its details are fetched with an HTTP request and displayed in `<ContactDetails>`.

* Before User selects a matching contact and during HTTP request for details of every chosen contact, `<Placeholder>` is shown instead of contact details. 

* If any error happens during details fetch (eg. because of `404 Not Found` response for invalid contact ID), `<FetchFailure>` appears instead of contact details, until next fetch request.

* Successfully fetched contact details are rendered: name, phone, and address.


## Setup

Follow these steps if you are using zip/git mode (i.e. not available inside Devskiller in-browser IDE):

1. `npm install` – install dependencies
2. `npm test` – run all tests (this will be used to evaluate your solutions)
3. `npm run test:watch` – run all tests in _watch mode_ (alternative to `npm test` which you might find more convenient to use locally)
4. `npm start` – (optional) serve the application locally at [http://localhost:3000/](http://localhost:3000/) (it won't be used to evaluate your solutions)
5. `nvm install` - (optional) set up the expected _major_ version of Node.js locally ([`nvm`](https://github.com/nvm-sh/nvm) required; Node.js version defined in `.nvmrc` file)

This application was generated using [Create React App](https://github.com/facebook/create-react-app). It has all the standard setups.

