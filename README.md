# Template for a Web Components project

## Installation

This project template uses Yarn 2 in [Zero-Installs](https://yarnpkg.com/features/zero-installs)
mode, so there is no initial installation required aside from cloning or forking the repo - just run
`yarn start` to spin up the Hello World app.

Note that when you change the package name to begin your own coding project, you will need to
`yarn install` to have that name change reflected in the yarn lockfile, otherwise you'll get an
error on `yarn start`. However, committing the resulting changes will then mean that others
cloning and running your app will not need to `yarn install`.

You can opt out of Zero-Installs if you wish; see the above link for more info. You will need to
modify the `.gitignore` as well. You can also revert to Yarn 1 if you wish, although Yarn wouldn't
recommend that :)

## Run (developer mode)

* `yarn start`
* visit `http://localhost:8080`

## Build and Run (production mode)

* `yarn build`
* `yarn dlx serve dist`
* visit `http://localhost:5000`

## Further thoughts
I have included a literal "template" tag for generating and cloning a template element, to remove
some common boilerplate code. However, there is far more that could be done. Repetitive boilerplate
for creating Custom Elements and configuring their behaviour can be avoided by using a third-party
library. Popular examples include:

### [LitElement](https://lit-element.polymer-project.org/)

LitElement is a class-based library for Custom Elements. It provides its own custom attribute syntax
for binding event handlers and values to a Custom Element and its attributes, and it also has a
number of rules and configuration settings for property-attribute binding and when updates occur.
All of which basically makes LitElement _yet another framework_ .... Yikes!

### [Hybrids](https://github.com/hybridsjs/hybrids)
 
In contrast to most other Custom Element helper libraries, Hybrids takes a _functional_ approach to
defining Custom Elements. Again there's a new API to learn, but it's not too arduous. Unlike other
libraries, Hybrids recommends only using html attributes for static, initialization-time config
values, and to use property setters/getters for everything else; this avoids any overhead in
converting objects to/from JSON strings.
