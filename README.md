# Augmented Reality Demo

[View Live Demo Here ↗](https://wsoeltz.github.io/ar-demo/)

This is a simple demo of running AR.js with A-Frame to render text a lat/lng location.

## Running and testing the project locally

To run this project locally, first pull this repo. If you have Node/NPM installed you can install the following two packages globally:

```bash
npm install --global http-server ngrok
```

Once those are installed, open two terminal windows at the root of the project directory. In the first window run:

```bash
npm start
```

This will boot up a local http-server at localhost:3000 and watch for changes. Then in the second window run:

```bash
npm run forward
```

This will now forward your local server to an actual web server via ngrok. The terminal window should give you a url for `https`. You can now access this url on your phone in order to test changes via your mobile device. `https` is required for the web application to use the device's camera

## Making changes

The only source file that needs to be edited is `index.html`. In there contains the scene for the app to run.

## Further documentation

For further modifications, look into the AR.js and A-Frame documentation -

- [A-Frame](https://aframe.io/docs/1.2.0/introduction/)
- [AR.js](https://ar-js-org.github.io/AR.js-Docs/)

