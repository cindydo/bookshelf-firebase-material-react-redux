# Bookshelf (Firebase, Material UI, React, and Redux)
Bookshelf is an app that helps users keep track of books they have read. This project used https://github.com/r-park/todo-react-redux.git as a starting point, but has been modified heavily to incorporate Material UI and other features.

Try the demo at https://bookshelf-eb64e.firebaseapp.com.

## Features
- Google sign-in and authentication
- Ability to add, edit, or delete books
- Ability to undelete a book
- Ability to rate books (on a scale of 1 to 5 stars)
- Ability to mark a book as private or public
- Material UI

## Installation and Running
Run `npm install` and then `npm run dev` to start the webpack development server running on `localhost:3000`

## Deploying to Firebase
#### Prerequisites:
- Create a free Firebase account at https://firebase.google.com
- Create a project from your [Firebase account console](https://console.firebase.google.com)
- Configure the authentication providers for your Firebase project from your Firebase account console

#### Configure this app with your project-specific details:
```javascript
// .firebaserc

{
  "projects": {
    "default": "your-project-id"
  }
}
```
```javascript
// src/core/firebase/config.js

export const firebaseConfig = {
  apiKey: 'your api key',
  authDomain: 'your-project-id.firebaseapp.com',
  databaseURL: 'https://your-project-id.firebaseio.com',
  storageBucket: 'your-project-id.appspot.com'
};
```

#### Install firebase-tools:
```shell
$ npm install -g firebase-tools
```

#### Build and deploy the app:
```shell
$ npm run build
$ firebase login
$ firebase use default
$ firebase deploy
```
