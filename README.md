# clickeygame



This project was bootstrapped with Create React App.

Below you will find some information on how to perform common tasks.
You can find the most recent version of this guide here.

Table of Contents
Updating to New Releases
Sending Feedback
Folder Structure
Available Scripts
npm start
npm test
npm run build
npm run eject
Supported Browsers
Supported Language Features and Polyfills
Syntax Highlighting in the Editor
Displaying Lint Output in the Editor
Debugging in the Editor
Formatting Code Automatically
Changing the Page <title>
Installing a Dependency
Importing a Component
Code Splitting
Adding a Stylesheet
Post-Processing CSS
Adding a CSS Preprocessor (Sass, Less etc.)
Adding Images, Fonts, and Files
Using the public Folder
Changing the HTML
Adding Assets Outside of the Module System
When to Use the public Folder
Using Global Variables
Adding Bootstrap
Using a Custom Theme
Adding Flow
Adding a Router
Adding Custom Environment Variables
Referencing Environment Variables in the HTML
Adding Temporary Environment Variables In Your Shell
Adding Development Environment Variables In .env
Can I Use Decorators?
Fetching Data with AJAX Requests
Integrating with an API Backend
Node
Ruby on Rails
Proxying API Requests in Development
"Invalid Host Header" Errors After Configuring Proxy
Configuring the Proxy Manually
Configuring a WebSocket Proxy
Using HTTPS in Development
Generating Dynamic <meta> Tags on the Server
Pre-Rendering into Static HTML Files
Injecting Data from the Server into the Page
Running Tests
Filename Conventions
Command Line Interface
Version Control Integration
Writing Tests
Testing Components
Using Third Party Assertion Libraries
Initializing Test Environment
Focusing and Excluding Tests
Coverage Reporting
Continuous Integration
Disabling jsdom
Snapshot Testing
Editor Integration
Debugging Tests
Debugging Tests in Chrome
Debugging Tests in Visual Studio Code
Developing Components in Isolation
Getting Started with Storybook
Getting Started with Styleguidist
Publishing Components to npm
Making a Progressive Web App
Opting Out of Caching
Offline-First Considerations
Progressive Web App Metadata
Analyzing the Bundle Size
Deployment
Static Server
Other Solutions
Serving Apps with Client-Side Routing
Building for Relative Paths
Azure
Firebase
GitHub Pages
Heroku
Netlify
Now
S3 and CloudFront
Surge
Advanced Configuration
Troubleshooting
npm start doesn’t detect changes
npm test hangs on macOS Sierra
npm run build exits too early
npm run build fails on Heroku
npm run build fails to minify
Moment.js locales are missing
Alternatives to Ejecting
Something Missing?
Updating to New Releases
Create React App is divided into two packages:

create-react-app is a global command-line utility that you use to create new projects.
react-scripts is a development dependency in the generated projects (including this one).
You almost never need to update create-react-app itself: it delegates all the setup to react-scripts.

When you run create-react-app, it always creates the project with the latest version of react-scripts so you’ll get all the new features and improvements in newly created apps automatically.

To update an existing project to a new version of react-scripts, open the changelog, find the version you’re currently on (check package.json in this folder if you’re not sure), and apply the migration instructions for the newer versions.

In most cases bumping the react-scripts version in package.json and running npm install in this folder should be enough, but it’s good to consult the changelog for potential breaking changes.

We commit to keeping the breaking changes minimal so you can upgrade react-scripts painlessly.

Sending Feedback
We are always open to your feedback.

Folder Structure
After creation, your project should look like this:

my-app/
  README.md
  node_modules/
  package.json
  public/
    index.html
    favicon.ico
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
For the project to build, these files must exist with exact filenames:

public/index.html is the page template;
src/index.js is the JavaScript entry point.
You can delete or rename the other files.

You may create subdirectories inside src. For faster rebuilds, only files inside src are processed by Webpack.
You need to put any JS and CSS files inside src, otherwise Webpack won’t see them.

Only files inside public can be used from public/index.html.
Read instructions below for using assets from JavaScript and HTML.

You can, however, create more top-level directories.
They will not be included in the production build so you can use them for things like documentation.

Available Scripts
In the project directory, you can run:

npm start
Runs the app in the development mode.
Open http://localhost:3000 to view it in the browser.

The page will reload if you make edits.
You will also see any lint errors in the console.

npm test
Launches the test runner in the interactive watch mode.
See the section about running tests for more information.

npm run build
Builds the app for production to the build folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.
Your app is ready to be deployed!

See the section about deployment for more information.

npm run eject
Note: this is a one-way operation. Once you eject, you can’t go back!

If you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except eject will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use eject. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

Supported Browsers
By default, the generated project uses the latest version of React.

You can refer to the React documentation for more information about supported browsers.

Supported Language Features and Polyfills
This project supports a superset of the latest JavaScript standard.
In addition to ES6 syntax features, it also supports:

Exponentiation Operator (ES2016).
Async/await (ES2017).
Object Rest/Spread Properties (stage 3 proposal).
Dynamic import() (stage 3 proposal)
Class Fields and Static Properties (part of stage 3 proposal).
JSX and Flow syntax.
Learn more about different proposal stages.

While we recommend using experimental proposals with some caution, Facebook heavily uses these features in the product code, so we intend to provide codemods if any of these proposals change in the future.

Note that the project only includes a few ES6 polyfills:

Object.assign() via object-assign.
Promise via promise.
fetch() via whatwg-fetch.
If you use any other ES6+ features that need runtime support (such as Array.from() or Symbol), make sure you are including the appropriate polyfills manually, or that the browsers you are targeting already support them.

Also note that using some newer syntax features like for...of or [...nonArrayValue] causes Babel to emit code that depends on ES6 runtime features and might not work without a polyfill. When in doubt, use Babel REPL to see what any specific syntax compiles down to.

Syntax Highlighting in the Editor
To configure the syntax highlighting in your favorite text editor, head to the relevant Babel documentation page and follow the instructions. Some of the most popular editors are covered.

Displaying Lint Output in the Editor
Note: this feature is available with react-scripts@0.2.0 and higher.
It also only works with npm 3 or higher.

Some editors, including Sublime Text, Atom, and Visual Studio Code, provide plugins for ESLint.

They are not required for linting. You should see the linter output right in your terminal as well as the browser console. However, if you prefer the lint results to appear right in your editor, there are some extra steps you can do.

You would need to install an ESLint plugin for your editor first. Then, add a file called .eslintrc to the project root:

{
  "extends": "react-app"
}
Now your editor should report the linting warnings.

Note that even if you edit your .eslintrc file further, these changes will only affect the editor integration. They won’t affect the terminal and in-browser lint output. This is because Create React App intentionally provides a minimal set of rules that find common mistakes.

If you want to enforce a coding style for your project, consider using Prettier instead of ESLint style rules.

Debugging in the Editor
This feature is currently only supported by Visual Studio Code and WebStorm.

Visual Studio Code and WebStorm support debugging out of the box with Create React App. This enables you as a developer to write and debug your React code without leaving the editor, and most importantly it enables you to have a continuous development workflow, where context switching is minimal, as you don’t have to switch between tools.

Visual Studio Code
You would need to have the latest version of VS Code and VS Code Chrome Debugger Extension installed.

Then add the block below to your launch.json file and put it inside the .vscode folder in your app’s root directory.

{
  "version": "0.2.0",
  "configurations": [{
    "name": "Chrome",
    "type": "chrome",
    "request": "launch",
    "url": "http://localhost:3000",
    "webRoot": "${workspaceRoot}/src",
    "sourceMapPathOverrides": {
      "webpack:///src/*": "${webRoot}/*"
    }
  }]
}
Note: the URL may be different if you've made adjustments via the HOST or PORT environment variables.

Start your app by running npm start, and start debugging in VS Code by pressing F5 or by clicking the green debug icon. You can now write code, set breakpoints, make changes to the code, and debug your newly modified code—all from your editor.

Having problems with VS Code Debugging? Please see their troubleshooting guide.

WebStorm
You would need to have WebStorm and JetBrains IDE Support Chrome extension installed.

In the WebStorm menu Run select Edit Configurations.... Then click + and select JavaScript Debug. Paste http://localhost:3000 into the URL field and save the configuration.

Note: the URL may be different if you've made adjustments via the HOST or PORT environment variables.

Start your app by running npm start, then press ^D on macOS or F9 on Windows and Linux or click the green debug icon to start debugging in WebStorm.

The same way you can debug your application in IntelliJ IDEA Ultimate, PhpStorm, PyCharm Pro, and RubyMine.

Formatting Code Automatically
Prettier is an opinionated code formatter with support for JavaScript, CSS and JSON. With Prettier you can format the code you write automatically to ensure a code style within your project. See the Prettier's GitHub page for more information, and look at this page to see it in action.

To format our code whenever we make a commit in git, we need to install the following dependencies:

npm install --save husky lint-staged prettier
Alternatively you may use yarn:

yarn add husky lint-staged prettier
husky makes it easy to use githooks as if they are npm scripts.
lint-staged allows us to run scripts on staged files in git. See this blog post about lint-staged to learn more about it.
prettier is the JavaScript formatter we will run before commits.
Now we can make sure every file is formatted correctly by adding a few lines to the package.json in the project root.

Add the following line to scripts section:

  "scripts": {
+   "precommit": "lint-staged",
    "start": "react-scripts start",
    "build": "react-scripts build",
Next we add a 'lint-staged' field to the package.json, for example:

  "dependencies": {
    // ...
  },
+ "lint-staged": {
+   "src/**/*.{js,jsx,json,css}": [
+     "prettier --single-quote --write",
+     "git add"
+   ]
+ },
  "scripts": {
Now, whenever you make a commit, Prettier will format the changed files automatically. You can also run ./node_modules/.bin/prettier --single-quote --write "src/**/*.{js,jsx,json,css}" to format your entire project for the first time.

Next you might want to integrate Prettier in your favorite editor. Read the section on Editor Integration on the Prettier GitHub page.

Changing the Page <title>
You can find the source HTML file in the public folder of the generated project. You may edit the <title> tag in it to change the title from “React App” to anything else.

Note that normally you wouldn’t edit files in the public folder very often. For example, adding a stylesheet is done without touching the HTML.

If you need to dynamically update the page title based on the content, you can use the browser document.title API. For more complex scenarios when you want to change the title from React components, you can use React Helmet, a third party library.

If you use a custom server for your app in production and want to modify the title before it gets sent to the browser, you can follow advice in this section. Alternatively, you can pre-build each page as a static HTML file which then loads the JavaScript bundle, which is covered here.

Installing a Dependency
The generated project includes React and ReactDOM as dependencies. It also includes a set of scripts used by Create React App as a development dependency. You may install other dependencies (for example, React Router) with npm:

npm install --save react-router
Alternatively you may use yarn:

yarn add react-router
This works for any library, not just react-router.

Importing a Component
This project setup supports ES6 modules thanks to Babel.
While you can still use require() and module.exports, we encourage you to use import and export instead.
