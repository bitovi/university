@page learn-react/setting-up-environment Setting up your environment
@parent learn-react 1

@description Learn how to setup a react environment using create-react-app

@body

## What is React?

In a nutshell, React is a frontend JavaScript library which makes it very easy to build scalable apps.

While it's most commonly used for building web apps, React can also be used to create mobile & desktop apps (this requires additional libraries).

React is concerned with allowing developers to break the view layer of their apps into small, re-usable chunks called Components. These components can be rendered by React onto the browser and will automatically update whenever the data in your app changes (we call this data state).

One of the best things about React is that it can be used in any website, even one that is already build with another framework. This makes it easy to convert an existing app to React, or just use React for one part of a site.

### The React Stack

In it's simplest form React is just a library, but when developing real world applications, React is best used in combination with a number of other technologies. Let's take a look at some of these below:

- **Babel** - Babel is a JavaScript transcompiler which allows developers to use the latest ECMAScript features in a backwards compatible way. React relies on Babel specifically to transpile JSX (the syntax used to define component layouts) into executable JavaScript code.
- **Webpack** - Webpack let's developers bundle their React components/apps into small, easily servable bundles which can be downloaded and run when the user's webpage loads. Webpack configurations also allow for live-reloading sites in development.
- **Jest** - Jest is one of the most popular testing libraries in all of JavaScrpt, and can be used to test React components very easily. 

In addition to the three highlighted above, there are many more small libraries/technologies which make developing in React much easier.

While it's possible to set up a codebase yourself which integrates all of these things together, there is actually a way of generating a pre-configured codebase with all of these things built into it called Create React App.

## Create React App

Create React App is a nodejs package created by Facebook (creators of React) which gives developers the ability to scaffold out pre-configured React apps that automatically follow industry best practices.

It also acts as a sort of standard for how React apps should be structured and organized. For example, most professional React developers could jump into a codebase generated by Create React App and feel right at home (with the configurations/commands that is).

Create React App can be installed via nodejs as a global dependency:

```bash
npm install -g create-react-app
```

Once installed, you can create an app using the new command (note you can also run this with `npx`)

```bash
create-react-app myapp
cd myapp
```

The above will create a new app called `newapp` in a folder with the same name.

### Looking at Our Generated Project

Let's walk through some of the files that were generated.

```code
├── node_modules
├── public/
├── src/
├── .gitignore
├── package.json
├── README.md
├── yarn.lock
```

**/public**

The public folder contains static files which will eventually be served up as part of your website. The most important file here is `index.html`, this is the file React will "hook into" and render all of it's contents to.

You can also include global css files here along with any images and other static HTML files.

Generally however, you shouldn't need to touch this folder too much.

**/src**

The `src` folder is where you'll store all your React components and generally just all of the code for your app. This should already be seeded with an small sample app (you can safely delete anything), but the most important file is `index.js`.

It's in `index.js` where our React app is initialized and we attach it to `index.html`.

**package.json**

The `package.json` file is intentionally very small, there are only a few dependencies included by default.

The most important thing here are the scripts:

```json
"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
},
```

Create React App provides a set of scripts (`react-scripts`) which know how to start, build and test your app. It's generally recommended to leave these as-is, a lot of work has been put into these scripts to ensure the best developer experience possible.

The final script included, `eject` is very important. Create React App, by default, will hide all of the configuration files and the transitive dependencies (Webpack, Babel, EsLint, etc). If you run the `eject` command all of these will be dumped into your project, giving you full control.

> Note that it's generally recommend **not** to eject unless you absolutely have to.

## Version Control & Deployment

Create React App will automatically initialize the new folder as a git repo, which can be checked into source control just like any other project.

One of the benefits of using `react-scripts` is it's great build process. When you run the `npm run build` command, your site will automatically be bundled, minified, and dumped into a `build` folder. 

This folder can now be uploaded to any web-server and served statically just like a normal HTML website, no fancy webserver or processes needed.