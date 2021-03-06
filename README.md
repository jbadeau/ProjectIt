[![Build Status](https://travis-ci.org/projectit-org/ProjectIt.svg?branch=development)](https://travis-ci.org/projectit-org/ProjectIt)

# ProjectIt
Projectional Editor for the Web.

ProjectIt will be presented at the LangDev workshop in Amsterdam on March 21-22.

![logo](/public/images/projectit-logo-3d.png)

**Note**. This project is Work in Progress, no dirstribution has been made yet. No version numer is attached yet, the first 0.? release will be later this year.

## What is ProjectIt

ProjectIt is a TypeScript/JavaScript framework to create and implement projectional editors for Domain-Specific Languages (DSLs) with.

It is mostly unopinionated with regards to the models that can be projected, as long as you can make it observed using [MobX](https://mobx.js.org/).
The framework provides an internal projection DSL to specify layouts and typical editor behaviour.
It's the job of the developer of the projectional editor to map models to that projection DSL.
The framework provides standard functionality mostly for navigating in the editor, but also for deleting model elements.

ProjectIt provides full support for editing expressions with associativity and precedences.

For creating elements  the DSL implementor needs to 
provide callbacks for manipulating the state of the model based on actions in the editor.

Note: no model (persistence) infrastructure is provided.

## Installation

The main prerequisites are: [Node.js](https://nodejs.org/) and [yarn](https://yarnpkg.com/).
We are typically using the latest versions of both, although older versions likely work just as well.
You could also try and use NPM instead of yarn.

To install all dependencies:

    yarn install

To build and run the demo locally:

    yarn build
    yarn start

To build and run the docs locally:

    yarn start:docs
    
This will open a browser with the demo app on `http://localhost:3000/`.
The demo app is work in progress.

At the moment, the following are non-existent:

* a distributable NPM package,
* tests,
* documentation,
* CI.

## Source organisation

* `.idea`: workspace files for the JetBrains' WebStorm that we use.
* `.vscode`: workspace files for the Visual Studio Code IDEs that we use (to be done).
* `dist`: target directory for WebPack.
* `projectit/src`: framework source code.
* `projectit/doc`: documentation
* `projectit-demo`: source code using the framework to implement a projectional editor for the demo language.
    The main entry point is `projectit-demo/src/run.ts`.
* `projectit-meta`: source code using the framework to implement a projectional editor for an experimental meta language..
* `projectit-model`: source codefor decorators that can be used to easily implement a language that can be directly used by ProjectIt.
* `/*`: the usual suspects.

