# Personal Academic Website

This is a personal academic website built on top of a Google Sheet document that is super easy to maintain.

This website at [https://cecilia322.github.io](https://cecilia322.github.io) is serving contents in [this Google Sheets document](https://docs.google.com/spreadsheets/d/e/2PACX-1vQqPZmK_4NyfVjo90k7svizGG6W5daZkgdBbLYRJpux9jKANeRh9dYi7K1BTV1diQ/pubhtml) and you don't even have to do anything to reflect the change to the website after editing the contents of this document. 

Fork this project and have your own website!

## How does this work?

This vue.js based web application served as Github Pages dynamically fetches the contents of the Google Sheets document on the client's side, using Google Sheets API. 
No actual contents are stored in this repository.

## How to fork and get your own website

1. Fork this repository to your account and rename it as "*{your-github-username}*.github.io". 

1. Create your own Google Sheets document, copy and paste the contents of [this sheets document](https://docs.google.com/spreadsheets/d/e/2PACX-1vQqPZmK_4NyfVjo90k7svizGG6W5daZkgdBbLYRJpux9jKANeRh9dYi7K1BTV1diQ/pubhtml). Make sure to get all sheets in the document prepared. 

1. Set your document's sharing settings as: *Public on the web - Anyone on the Internet can find and view*.

1. Get your document id from the URL of the document. Set it as the value of `googleSheetDocId` in `./config.js`.

1. Create a new Google account that you are only going to use for this website, get an API key that belongs to your new Google account. Check out on [this answer on Stack Overflow](https://stackoverflow.com/a/46583300) if you don't know how to get an API key for a Google account. Set it as the value of `googleApiKey` in `./config.js`. 

1. Edit contents of your own Google Sheets document to change the contents of your website at *https://{your-github-username}.github.io*. 

Now your website is up and ready!

## Development

Just in case if you are interested in modifying this web application. 

### Dependencies

Make sure to install [Node.js](https://nodejs.org/en/) and [Yarn](https://yarnpkg.com/en/) on your environment before you start working on this project.

Install Node.js dependencies with the following command.

```bash
$ yarn install
```

### Commands

Following commands are available for development. 

```bash
# build for production
$ yarn build

# development mode
$ yarn dev

# run unit tests
$ yarn test

# serve the bundled dist folder in production mode
$ yarn serve
```

### Polyfills

By default we only polyfill `window.Promise` and `Object.assign`. You can add more polyfills in `./src/polyfills.js`.

### Analyze bundle size

Run `yarn report` to get a report of bundle size.

---

This project is generated by [create-vue-app](https://github.com/vue-land/create-vue-app).
