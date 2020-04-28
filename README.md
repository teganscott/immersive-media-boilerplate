### Project includes three.js, tone.js, firebase-tools, firebase hosting and materialize CSS libraries

## Installation

    git clone https://github.com/ianpetrarca/immersive-media-boilerplate
    cd immerisve-media-boilerplate
    npm install

## File Structure + Descriptions

    ├── build                  # Webpack Production build output 
    ├── src                    # Source files
        ├── components         # Folder for  components (JS)
        └── templates          # Folder for resuseable html (HTML)
    ├── .firebaserc            # Connects your project to Firebase Hosting 
    ├── firebase.json          # Specifies which directory to upload to Firebase
    ├── package.json           # NPM 
    ├── webpack.config.js      # Webpack Config file for dev server/production builds
    
## Development Stage

To spin up a localhost site, run the following command then point a WebVR friendly browser to http://localhost:8080/

    npm run dev

To view the dev server on an external device find out your local IP address (Type 'ipconfig' in any terminal) and view the 8080 port. This may look like:

    192.168.1.165:8080

 **WebVR-Boilerplate was designed for Single-Page-Applications** and does not handle multiple html files without reconfiguring the _webpack.config.js_ HTMLWebpack plugin.
 
 ## Building 
 
 To build and optimze your HTML/JS run:
     
     npm run build
 
 This will Webpack build your ./src folder into the ./build directory with the specifications made in the _webpack.config.js_ file.

## Deploying

WebVR-Boilerplate uses Firebase for quick and easy static-asset hosting. If you haven't already, install Firebase by running:

    npm install -g firebase-tools
    
After installing Firebase, run _init_ and setup a hosting connection:

    firebase init 
    
The _firebase.json_ file tells Firebase Hosting to use the _./build directory. Find out more about Firebase Hosting [Here](https://firebase.google.com/docs/hosting/quickstart)

Once Firebase is installed and initialized, run the following code to build and deploy your code:

    npm run deploy
    
