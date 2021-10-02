# Augmented Reality Demo

[View Live Demo Here ↗](https://wsoeltz.github.io/ar-demo/)

This is a simple demo of running AR.js with A-Frame to render text next to common grocery store items in a browser based web application.

After opening the demo on your phone, please wait until the loading screen goes away before pointing the camera at the objects/image markers. It may take a bit of moving the phone around before it is able to recognize the first object or marker. This seems to be a bit of an issue with the platform itself, all other examples I came across had similar lag.

The program is able to recognize the following images. If you have these exact products (with the same exact label) in your house, you can try getting the app to recognize them based on the label itself! Otherwise you should be able to point your phone at the following images to see it in action:

### Olive Oil:

![Olive Oil](https://github.com/wsoeltz/ar-demo/blob/main/assets/olive-oil.png?raw=true)

---

### Wheat Thins:

![Wheat Thins](https://github.com/wsoeltz/ar-demo/blob/main/assets/wheat-thins.png?raw=true)

---

### Salt:

![Salt](https://github.com/wsoeltz/ar-demo/blob/main/assets/salt.png?raw=true)

---

### Flour:

![Flour](https://github.com/wsoeltz/ar-demo/blob/main/assets/flour.png?raw=true)

---

### Soy Sauce:

![Soy Sauce](https://github.com/wsoeltz/ar-demo/blob/main/assets/soy-sauce.png?raw=true)


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

The only source file that needs to be edited is `index.html`. In there contains the scene and reference to all of the markers for the app to run. Within the `assets` directory includes all of the image markers, which are NFTs (as is required by AR.js).

To add a new NFT, first create an image file that you want use. Then use [this online tool](https://carnaux.github.io/NFT-Marker-Creator/#/) to convert it into an NFT. After some time (seconds to minutes), it will prompt you to download three files. Save all three along with the original source image in the `assets` folder. You can now add another marker in the `index.html` at the bottom of the list of other markers, replacing `{ASSET-NAME}` with the name of your asset (without any extension) and `{TEXT}` with your desired text -

```html
  <a-nft type="nft"
    url="./assets/{ASSET-NAME}"
    smooth="true" smoothCount="10" smoothTolerance=".01" smoothThreshold="5">
    <a-entity text-geometry="value: {TEXT}" material="color: white" scale="18 18 18" position="0 0 -20" rotation="-120 0">
  </a-nft>
```

## Further documentation

For further modifications, look into the AR.js and A-Frame documentation -

- [A-Frame](https://aframe.io/docs/1.2.0/introduction/)
- [AR.js](https://ar-js-org.github.io/AR.js-Docs/)

## Working example screenshots

Here are some screenshots taken of the app working for each of the original 5 images -

![Olive Oil](https://github.com/wsoeltz/ar-demo/blob/main/assets/examples/olive-oil.jpg?raw=true)

![Wheat Thins](https://github.com/wsoeltz/ar-demo/blob/main/assets/examples/wheat-thins.jpg?raw=true)

![Salt](https://github.com/wsoeltz/ar-demo/blob/main/assets/examples/salt.jpg?raw=true)

![Flour](https://github.com/wsoeltz/ar-demo/blob/main/assets/examples/flour.jpg?raw=true)

![Soy Sauce](https://github.com/wsoeltz/ar-demo/blob/main/assets/examples/soy-sauce.jpg?raw=true)
