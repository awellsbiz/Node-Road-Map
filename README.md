## NODE RODE MAP

# ABOUT

- Building an app using Node with Express: you are on the rode to bulding a full stack web application from the ground up! This README includes some inportant information and are the steps to take in order to get started. 

# WHAT IS NODE?

- Node Gives us a server-side enviroment that can handle logic written in JS + allows it to be ran on a server.

- You can install Node via Hombrew. Goodle how to do so. Or check GA gitbook!

# STEPS FOR INSTAL AND 

1. Make a directory (via termina- mkdir) or open up directory if you have cloned from github.

2. Change directory (via terminal use cd) in to the folder and Initialize in side the folder by bashing npm init

3. make your entry point  by touchin a file usually touch index.js via the terminal. write some code for test like console.log("hello world")

4. run your program in the terminal for test: node [file name(index.js)]

## NODE MODULES

- Node's module system allows code written in one file to be exported, and then imported into other files. By importing a module (i.e. a specified section of code), we can then use that code as if it actually were written in the file we imported it to.

- Node.js comes with a set of built-in modules that we can use in our code without having to install them. To do this, we need to require the module using the require keyword and assign the result to a variable. This can then be used to invoke any methods the module exposes.

1. module.exports is an object that will hold the code to be exported. We can use dot-notation to add the code we want to export to this object: module.exports.beBasic = () => console.log("That's so fetch!")

2. Then We got to unpack the module to use it in other files through the require function- its specific to node. This function takes one argument: the path to the file that contains the module you are exporting: 
const myModule = require('./myModule.js'(the file that we created)/ or 'express');
myModule.beBasic();

you can run it through command line in terminal with 'node index.js'

## NODE PACKAGES (NPM)

- Core modules are great for gaining quick access to commonly-needed functionality in your program, and local modules allow you the flexibility to build out whatever tools you might possibly need, but third party modules, which fall somewhere in between, are perhaps the most exciting modules of them all!

- We can use nodemon (a built in package that makes developing node apps eaiser. it resets the app every time we make a change.) We installed it globally since we are using it alot. once we access the foler we want to work in we can bash nodemon to fire it up. 

- when using a third party module use 'npm i [install what you want]' inside the terminal
- then open up a index. js file and open up the libray by making a variable and using require().

- when you is npm install command dont forget to set ignore files for modules. We dont need to have the node_modules folder to be tracked by git all the time( takes up space- can cause errors during deployment) & we can just re-install the packages that we need. So, by using .gitignore will make a file of everything we should not be tracking .gitignore >> node_modules in the directory that we have installed the modules.

- ports are end points of communication. We use 3000 or 8000 define a variable and set it.

## CHEAT SHEET

- once you craete a new project:
bring in enviroment using require() and set a variable
import express
create application object using express as a value
define a port variable from enviroment with a default value (3000, 8000)
then do your middleware and routes: const middlewareFunction = (req, res) => {
 console.log("This is middleware")
}
server listener goes last- or else it wont run correctly app.listen(PORT, ()=>{ console.log(`listen on port ${PORT}`)})