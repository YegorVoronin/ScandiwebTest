First I downloaded and setup webpack 
(I usually don't use Webpack, and prefer to use just React with libraries)
SETUP
    1) First I downloaded all the dependencies
        -I used the "npm -init" to create the package.json file.
        -Then I installed the "react" and "react-dom" dependencies
        -then I setup the other development dependencies 
            (for things like SASS, loaders, and Babel)
        -then I created a .babelrc to create presets that will be used.
    2) Create the webpack configurations
        -I created a webpack.config.js file
        -in this file I created a path
        -then I created the module.exports and added the output property.
        -the files will go through the output property and this will pass 
            them through all the presets and loaders.
        -Inside the  property, I set up file named index.bundle.js
        -then I added a devServer property with a port of 3010 and made the browser 
        watch the content base and refresh when changed.
        -After that, I created a module property, adn created a rules 
            property with test to spot matching js or jsx files.
        -then, I added a "use", so when the files are found the computer 
            knows to use the babel-loader.
        - I also excluded the node modules just in case.
        -After that I created a multiple style loaders (style-loader, css-loader, 
            sass-loader), so SASS files can be used.
    3) Then start running the components
        -I create a source folder and in it the appropriate files, 
            like App.js, index.html, index.js, and App.scss
        - Then, I setup the App.js folder, by importing react, export the App, and
            adding the syntax
        -Then, I moved to index.html, and I created the place holders, and then made
            a div with an ID of 'app'.
        -now I use the React Dom to render the App component in index.js
        -In the index.html I reference the app ID, and added a script tag, 
            and sourced it to index.bundle.js
        -After that I opened the index.js, adn imported all needed usual components 
            and on top of those I imported the App component.
        -I added a require to loader, to load index.html 
        -then I went into package.json, and added new script command named 'serve'
        -then in the terminal I run 'npm run serve'
        -and it reminds me to install the web-pack-dev-server package, and I I let 
            it install through the terminal
        -Now I went to the browser and opened localhost 3010, and the dev server is up and runnning!
DEVELOPMENT
    1) I made a file named Carousel.js and Carousel.scss, which will be the core of my carousel.
    2) I went into the App.scss and made the background of the app cover the whole screen, and 
        made it grey, and used flexbox to align all items to the center.
    3) Now I exited all files except for Carousel.js and Carousel.scss
    4) In the Caroulel.js, I setup the the size of the carousel and split up the inside into the navigation
        and inner items
    5) Inside the navigation I create two buttons: "next" and "prev"
    6) I styled all of these options.
    4) I created an array with three string containing different hex codes, (This could also be an array of images, 
        but I decided to keep it simple).
    5) Then I created a useState, named slide and passed in a value of 0
    6) I styled the background of the "inner" div in the main Carousel.js file. I   
        I passed in the background as the first item in 'colors' array.
    7) Then I created a function called nextImg, this function is meant to move forward through the
        array of colors. 
    8) inside the function I set a if then statement, that will cycle through 
        all the images and restart once it got to the last one.
    9) Then I created the prevIMG function and it behaved the same way as
        the function nextIMG function but went to the previous picture.
MY FAILED FUNCTIONS
    I tried to create a swiping function, but I just couldn't figure it out.
    I understand how it works but I just don't know how to write it. 
    1) I would have to use a touchstart and touchend events. 
    2) During a touchstart event I would need to figure out where on the y
        axis is the finger touched, and get the value for that.
    3) Then I will need to figure out the y value on touch end.
    4) Then I can subtract the first value from the second to figure out 
        whether the swipe happened to the left or the right.
    5) So an if then statement to decide which way to swipe.
