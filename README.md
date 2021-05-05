# svelte
At the root level we have four folders and five files to begin with let's start with the important bits in package.json.

This file contains the dependencies and the scripts required for the project you can see that we are using swelt version 3 and that is listed as a dev dependency swelt is only used during the compilation phase and never bundled into the code that is sent to the browser we then have rollup which is a model bundler and a whole load of roller plug-ins listed as dev dependencies roll-up is responsible for transforming this weld code we write into JavaScript code that the browsers can understand 

there is one dependency which is the serve cli it allows us to run a static file server we also have three scripts dev for development built to create a production ready version of the application and start for the serv cli to serve the built application straightforward package.json file as you can see next we have the configuration file for rollup rollup.config.js this is the config file that is used when we run the command yarndev or yarn build if you're interested in the various configurations 

i recommend you take a look at roll up documentation next we have the yarn lock file based on whether you prefer npm or yarn as a package manager you're going to see yarn lock or package log files they simply ensure consistent installation of your dependencies and you don't really have to worry about them. 

We also have a git ignore and a readme file alright next let's talk about the folders the first one is node modules this is the folder in which all the dependencies are installed it is generated when you run the yarn command or npm install command the next folder is the public folder this folder contains static assets that are published when you want to go live with your application 

it contains three files we have a favicon which you see in the browser tab and is nothing spelled specific we also have a global css file which includes styles that are applied to our entire application and finally we have an index.html file which is the only html file you're going to have in your application 

we are building single page applications and this is it the view might dynamically change in the browser but it is this html file that gets served up typically you are not going to add any code in this file maybe some changes in the head tag but definitely not in the body tag you want swelt to control the ui and for that purpose we have a css and js file so slash build slash bundle.css slash build slash bundle.js these files are from the build folder which get generated when you run or build your application now 

please make a note of this empty body tag as we will come back to it shortly the next folder is the scripts folder which contains a file pertaining to typescript setup since we are going to learn swelt with just javascript we don't have to worry about this for now the final folder is the source folder which is the folder we will be working with the most during development the starting point for our swelt application is main.js 

in main.js we import the root component which is app component and invoke it as a function specifying the document body as the target element and if you can recollect we have an empty body element in our index.html file so everything inside this body tag will be managed by swelled for the hello world application the app component is rendered inside the body element that brings us to the app component which is present in app dot swelled now the dot swelled file extension

extension i bet is something new to you if you are learning about swelt for the first time. 

Let me tell you that it is a file where you specify the html css and javascript corresponding to a portion of the ui you see in the browser you can see here we have a script block with a variable called name for the html we have the main html tag with an h1 tag and a paragraph tag this is the text we see in the browser below the html we also have some styles specified within a style block the app.swelt file pretty much represents the ui you see in the browser so that is the folder structure of aswelt application created using the dkit command

next let's understand the control flow when you run this application in the terminal when you run the command yarn dev index.html file is served in the browser index.html contains a reference to bundle.js the bundle.js file is your main.js file compiled to a javascript format that the browser can understand he swelt code renders itself within the body tag

so if i inspect the heading element  you can see the main tag as a child of the body tag this is nothing but our app component the name of course is the name from main.js which gets replaced in the html because of the swelled compiler so hello name replace name with world which is hello world and that is what you see in the browser 

we will of course learn more about this swelt magic but this is pretty much the control flow from package.json dev script to index.html bundle.js script to main.js and finally app.swelt now i'm pretty sure this file extension which is dot swelt is new to you so let's discuss more about that 

