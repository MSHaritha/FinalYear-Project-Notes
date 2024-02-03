# FinalYearProject React-Notes 🚀


## Q: Difference between a `Library and Framework`?
A: A `library` is a collection of packages that perform specific operations whereas a `framework` contains the basic flow and architecture of an application. The major difference between them is the complexity. Libraries contain a number of methods that a developer can just call whenever they write code. React js is library and Angular is Framework.
The `framework` provides the flow of a software application and tells the developer what it needs and calls the code provided by the developer as required. If a `library` is used, the application calls the code from the library.


## Q: Why is `React known as React`?
A: `React` is named React because of its ability to `react to changes in data`.
React is called React because it was designed to be a declarative, efficient, and flexible JavaScript library for building user interfaces.
The name `React` was chosen because the library was designed to allow developers to "react" to changes in state and data within an application, and to update the user interface in a declarative and efficient manner.
`React` is a `JavaScript-based UI development library`. `Facebook` and an `open-source developer community` run it.


## Q: What is difference between `React and ReactDOM`?
A: `React` is a JavaScript library for building User Interfaces whereas `ReactDOM` is also JavaScript library that allows `React to interact with the DOM`.
The react package contains `React.createElement()`, `React.Component`, `React.Children`, and other helpers related to elements and component classes. You can think of these as the isomorphic or universal helpers that you need to build components. The react-dom package contains `ReactDOM.render()`, and in react-dom/server we have server-side rendering support with `ReactDOMServer.renderToString()` and `ReactDOMServer.renderToStaticMarkup()`.



## Q: What is difference between `react.development.js` and `react.production.js` files via `CDN`?
A: `Development` is the stage of an application before it's made public while `production` is the term used for the same application when it's made `public`.
`Development build` is several times (maybe 3-5x) `slower` than the `production build`.

## Q: What is `type="module"`?
```
<script type="module" src="main.js"></script>
```
As the name suggests, it allows you to import `modules`, which makes it easier to organize your code.
Enable `strict mode` by default. This makes your code run faster, and reports more runtime errors instead of silently ignoring them.
Execute your code only after the DOM has `initialized`, which makes DOM manipulation easier. Thanks to this, you won't need to listen to load/readystatechange/DOMContentLoaded events.
Prevent top level variables from implicitly polluting the global namespace.
Allow you to use top-level await in supported engines.
Load and parse your code `asynchronously`, which improves load performance.

# Steps  🚀
  - to dwnld parcel package
    ```
    npm i -D parcel
    ```
  - to dwnld react and react-dom
    ```
    npm i react
    npm i react-dom
    ```
  - to run using parcel in a localserver as a development build 
    ```
    npx parcel index.html 
    ```
  - write in top of app.js file
    ```
    import React from "react"
    import ReactDOM from "react-dom" 
    ```

    
# Explanations  🚀

# EP-02 Part-01 [ignating our app]  🚀
## Q:NPM
   - npm is basically a package manager that manages all the dependencies that you need during the project like parcel, express, node etc..,

> [!NOTE]
>package.json = configuration of project dependencies
>For example in package.json file:
> ```
>  "{
>      "name": "episode-02---igniting-our-app",
>      "version": "1.0.0",
>      "description": "learning react",
>      "main": "index.js",
>      "scripts": {
>        "test": "jest"
>      },
>      "keywords": [],
>      "git repository": "https://github.com/VasanthKumarTJ/Namste-React.git",
>      "author": "Vasanth Kumar",
>      "license": "ISC",
>      "devDependencies": {
>        "parcel": "^2.10.3"
>      }
>    }"
> ```

## Q:why do we need npm?
>   * our project is dependent on many packages, therefore npm will take care of these packages version basically it act as a configuration that have 
>   - package version EX: 
>    ```
>    "dependencies": {
>    "react": "^18.2.0",
>    "react-dom": "^18.2.0"
>    }
>  ```

> [!NOTE]
>## Q:types of dependencies a package can have
>    - ### learnt in namaste-react by akshay:
>        - DEV: generally required for development face (-D)
>        - NORMAL: used in production also
>
>    - ### others:
>        - peer dependencies.
>        - optional dependencies.
>        - bundled dependencies.


> [!IMPORTANT]
>## Q: install package with right depedencies
> ```
>   npm install -D parcel
> ```


## Q:Difference B/W (tilde) "~" and (caret) "^"
    - "~" will automatically updates to the next major version ex: version: 1.2 to 2.0
    - "^"  will auto update to next minor version ex: version 1.2 to 1.2.1

## Q:Transive dependencies
   - if you install parcel dependency package by typing "**npm i -D parcel**" then package parcel have other package that are needed so these folder therfore install another package and that package install another folder which are dependent, therefore the **node modules** folder have more folder plus the folder or package you installed like **parcel**

# EP-02 part-02 🚀

## Q: What is Parcel/Webpack? Why do we need it?
   - A: Parcel/Webpack is type of a web application bundler used for development and productions purposes or power our application     with different type functionalities and features. It offers blazing fast performance utilizing multicore processing, and requires   zero configuration. Parcel can take any type of file as an entry point, but an HTML or JavaScript file is a good place to   start. Parcel/ Webpack are type of bundlers that we use to power our application with different type functionalities and features.

## Parcel Features:
    - dev build
    - local server 
    - HMR (Hot Module Replacement) 
    - parcel keeps track of file changes via file watcher algorithm and renders the changes in the files
    - File watcher algorithm [ made with C++] 
    - caching [faster builds]
    - IMAGE optimization
    - Bundling
    - MINIFY in production build
    - compress
    - consistent hasing
    - code splitting
    - differential Bundling - support older browsers
    - Diagnostics
    - Gives better error suggestions
    - HTTPs
    - Tree Shaking - remove unused code for you
    - Diff bundles for DEV and Prod

# installation commands:
## Install:
   ```
   npm install -D parcel
   ```
   - D is used for development and as a development dependency.

## Q: what is npx
   - npx is like node  that executes the package and index.html file in the server so we can host the file in the server
   -  npx is a tool that is used to execute the packages. It comes with the npm, when you installed npm above 5.2.0 version then automatically npx will installed. It is an npm package runner that can execute any package that you want from the npm registry without even installing that package.

## Q: diff between "npx" and "npm"
   - npm means we are installing the package
   - npx means we are executing a particular package
   

## Parcel Commands :
   - for development build
     ```
     npx parcel <entry_point> 
     npx parcel index.html
     ```
  - For production build :
  - we have to remove the entry point in ``npm package.json, "main": App.js`` cause we use ``entry point`` in our parcel
    ```
    npx parcel build <entry_point> 
    ```

> [!IMPORTANT]
>## npm and react
>   - using react by cdn link is ``not prefereable`` because we make a network call to that link so we can get react but why do we need
to make netework call if we have react on our node modules 
>   - another advantage is ```we need update the link if another version of react comes``` but if we use npm the ```caret will update automatically```
>
>   ```
>   npm i react
>   npm i react-dom
>   ```
>   - even after installing react and react-dom as a package when  you run the server useing npx it will throw a errow saying react is not defined because we installed it but the file doest not know where React keyword coming from yet  so we have to import it using
>   ```
>   import React from "react"
>   import ReactDOM from "react-dom"
>   ```
>   - at the top☝


## Q: What is `.parcel-cache`?
A: `.parcel-cache` is used by parcel(bundler) to reduce the building time.
It stores information about your project when parcel builds it, so that when it rebuilds, it doesn't have to re-parse and re-analyze everything from scratch. It's a key reason why parcel can be so fast in development mode.


## Q: What is difference between `dependencies` vs `devDependencies`?
A: `Dependencies` should contain library and framework in which your app is built on, needs to function effectively. such as Vue, React, Angular, Express, JQuery and etc. 
`DevDependencies` should contain modules/packages a developer needs during development.
such as, `parcel, webpack, vite, mocha`.
`These packages` are `necessary only while you are developing your project`, not necessary on production.
To save a dependency as a devDependency on installation we need to do, 
```
npm install --save-dev
```
instead of just,
```
npm install --save
```


## Q: What is `Tree Shaking`?
A: `Tree shaking` is process of removing the unwanted code that we do not use while developing the application.
In computing, tree shaking is a dead code elimination technique that is applied when optimizing code.



## Q: List down your favorite `5 superpowers of Parcel` and describe any 3 of them in your own words.
A: `5 superpowers of Parcel`:
* `HMR (Hot Module Replacement)` - adds, or removes modules while an application is running, without a full reload.
* `File watcher algorithm` - File Watchers monitor directories on the file system and perform specific actions when desired files appear.
* `Minification` - Minification is the process of minimizing code and markup in your web pages and script files.
* `Image optimization`
* `Caching while development`


## Q: What is the difference between `package.json` and `package-lock.json`?
A: `package.json`:
* This file is mandatory for every project
* It contains basic information about the project
* Application name/version/scripts

`package-lock.json`:
* This file is automatically generated for those operations where npm modifies either the node_module tree or package-json.
* It is generated after an npm install
* It allows future devs & automated systems to download the same dependencies as the project.
* it also allows to go back to the past version of the dependencies without actual
‘committing the node_modules folder.
* It records the same version of the installed packages which allows to reinstall them.
Future installs will be capable of building identical description tree.

**~** or **^** in `package.json` file :
These are used with the versions of the package installed.

For example  in `package.json` file:
```
"dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  }
```

* **~** : `Approximately equivalent to version`, will update you to all future patch versions, without incrementing the minor version.
* **^** : `Compatible with version`, will update you to all future minor/patch versions, without incrementing the major version.

> If none of them is present, that means only the version specified in `package.json` file is used in the development.


## Q: Why should I not modify `package-lock.json`?
A: `package-lock.json` file contains the information about the dependencies and their versions used in the project. Deleting it would cause dependencies issues in the production environment. So don't modify it, It's being handled automatically by NPM.

## Q: What is `node_modules` ? Is it a good idea to push that on git?
A: `node_modules` folder like a cache for the external modules that your project depends upon. When you npm install them, they are downloaded from the web and copied into the node_modules folder and Nodejs is trained to look for them there when you import them (without a specific path).
`Don't push node_modules`in github because it contains lots of files(more than 100 MB), it will cost you memory space.


## Q: What is the `dist` folder?
A: The `/dist` folder contains the minimized version of the source code. The code present in the `/dist` folder is actually the code which is used on production web applications. Along with the minified code, the /dist folder also comprises of all the compiled modules that may or may not be used with other systems.


## Q: What is `browserslist`?
A: `Browserslist` is a tool that allows specifying which browsers should be supported in your frontend app by specifying "queries" in a config file. It's used by frameworks/libraries such as React, Angular and Vue, but it's not limited to them.
