# JATE - Just Another Text Editor

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)


![Example](/JATE-psa.gif)
  


## Table of Contents
- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Build Scripts](#build-scripts)
- [Testing and Validation](#testing-and-validation)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)

## Description

JATE (Just Another Text Editor) is a Progressive Web Application (PWA) designed to function as a feature-rich text editor. It is built to be fully functional offline, leveraging modern web technologies such as IndexedDB, service workers, and Webpack. JATE allows users to create, edit, and save text documents directly in the browser, with all changes automatically saved even when the application is not in focus. The application is also installable, providing a native app-like experience on desktop and mobile devices.

## Features

- **IndexedDB Integration**: JATE uses IndexedDB to store text data locally, ensuring persistence across sessions and when offline.
- **Offline Functionality**: The application works seamlessly without an internet connection, allowing users to continue editing their text documents offline.
- **Auto-Save Feature**: Content is automatically saved to IndexedDB when the DOM window loses focus, ensuring that no data is lost.
- **Bundled with Webpack**: The application is built and bundled using Webpack, optimizing the performance and loading of assets.
- **Service Worker with Workbox**: JATE uses a service worker created with Workbox to cache static assets, enabling fast load times and offline access.
- **Babel Integration**: The application is transpiled using Babel to support async/await and other modern JavaScript features, ensuring compatibility across different browsers.
- **PWA Capabilities**: JATE can be installed as a Progressive Web Application, providing a native app-like experience with offline functionality.
- **Manifest File**: A `manifest.json` file is automatically generated using the WebpackPwaManifest plugin, defining the application's metadata and icons for installation.

## Installation

To run JATE locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/jate.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd jate
   ```
3. **Install Dependencies**:
   ```bash
   npm install
   ```
4. **Start the Application**:
   ```bash
   npm run start
   ```

   This will start the backend server and serve the client application.

## Usage

1. **Running the Application**:
   - Run `npm run start` from the root directory. This command will bundle the JavaScript files using Webpack and start both the backend and frontend servers.
   - Open your browser and navigate to the application URL to access the text editor.

2. **Using the Text Editor**:
   - Enter your text in the editor. The content will be automatically saved to IndexedDB whenever the DOM window is unfocused.
   - Close and reopen the editor to see your previously saved content loaded from IndexedDB.

3. **Installing the PWA**:
   - Click on the "Install" button to download and install JATE as a Progressive Web Application on your desktop or mobile device.

4. **Offline Usage**:
   - Once installed, JATE can be used offline. All changes will be saved locally, and the service worker will cache static assets for faster loading.

## Deployment

JATE is deployed on Render and can be accessed at the following live URL:

- **Live URL**: [https://jate-text-editor-rmqh.onrender.com](https://jate-text-editor-rmqh.onrender.com)

To deploy the application yourself, ensure that you have the correct build scripts in place. The application should be built using Webpack before deployment.

## Build Scripts

- **Build the Application**:
  ```bash
  npm run build
  ```
  This command will bundle the application using Webpack, generating the HTML file, service worker, and manifest file.

- **Start the Development Server**:
  ```bash
  npm run start:dev
  ```
  This command runs the application in development mode with live reloading.

## Testing and Validation

- **No Errors on Load**: The application loads with no errors, and the text editor functions correctly in the browser.
- **Client-Server Structure**: The application follows a client-server folder structure, with separate directories for client and server code.
- **Service Worker Registration**: A service worker is registered using Workbox, with static assets pre-cached upon loading.
- **IndexedDB Integration**: Upon opening the text editor, IndexedDB is immediately created. Content is saved when the DOM window is unfocused and retrieved upon reopening the editor.
- **PWA Installation**: Users can install the web application as a PWA and use it offline.

## Contributing

Contributions to JATE are welcome! If you find any bugs or have suggestions for new features, feel free to open an issue or submit a pull request.

## Credits

Anamaris Ortiz 
GitHub: https://github.com/AnamarisOrtiz  
Email: anamarisortiz@hotmail.com

## License

This project is licensed under the MIT License.


