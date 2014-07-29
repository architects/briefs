# Concept Notes: Stylish.io

Stylish.io is a marketplace for high end, developer friendly UI kits and themes.  

The high end, developer friendly part will be made possible by an editor tool that allows front end developers / designers to:

- build a suite of third party dependencies / plugins
- customize a bootstrap or semantic-ui base to develop a theme
- edit / customize / preview components live in the browser
- combine components into blocks live in the browser
- combine blocks into page layouts live in the browser

The actual languages used for the templates and css will be preprocessor friendly:  

- haml / slim / jade
- less / sass
- coffeescript

## Inspirations

### Designmodo Startup Framework

[The startup framework](http://designmodo.com/startup) is a high end UI kit and landing page layout library.  

It is by far the highest quality distribution of bootstrap theme that I have ever worked with.  

Aside from the aesthetic, which may not be everyone's taste, the way the theme and templates themselves are broken up and distributed is really well done in a way which lends a lot of value to the work flows of the types of people who would use it.  

The startup framework is so well thought out as a theme, that the assets are extremely composable, and can be mixed and matched to great effect.  So much so, in fact, that they were able to build an interactive tool for doing so called the [The Generator](http://designmodo.com/generator)

I want the stylish theme editor to be a tool which empowers other people to build and distribute their own UI kits, following the same good structure of the Flat-UI theme, and Startup Framework, and with the same great documentation.

#### Block Structures in the Startup Framework 

The Designmodo startup framework is a collection of 'Blocks'. A Block is
a root level HTML element nested directly under the body tag, or in some
cases, a container element which is the only descendant of the body tag.

Blocks can be arbitrarily composed to generate a large number of landing page combinations.

The startup framework divides up their package into categories of blocks:

- headers
- footers
- content
- contacts
- prices
- projects
- crews

When you export something from the generator, it will give you the
markup for the blocks, as well as the css / less for that block. It will
wrap all of this up in a general HTML page which includes the global /
common / shared dependencies.


### CustomElements.io

CustomElements.io is a marketplace for HTML Components.  Stylish.io would be a marketplace for collections of HTML Components presented in different styles / themes

### Atom shell 

atom-shell allows me to use the same app core that github's atom editor
is based on.  allows me to distribute cross platform native apps while 
writing the UI in javascript, html, css.  also allows for running
sandboxed node.js backend code in the distributed executable.

### Codepen / JS Bin

The ability to live edit / preview code is crucial.  Especially with
support for preprocessors. Atom shell will lend itself to this. We could 
use grunt or gulp to handle the preprocessor step live / in watch mode. 

### Flat UI

Designmodo's Flat-UI is a great example of what somebody would be able
to produce with the Stylish framework and editor.  Stylish would provide
the organizational framework and editing workflow that likely went into 
whoever hand coded flat ui.

It is based on Bootstrap.  So in a sense, it is a bootstrap theme.
However unlike many other bootstrap themes, this is more generalized to
where it has more in common with bootstrap itself.

### Semantic UI

A great example of a component style guide, not based on the custom
elements or web components spec though.

### Bootstrap

Same as Semantic UI.

## Requirements

### Data Model

- Asset Manifests
  - third party dependencies / load order

- Blocks
  - uniquely named
  - can be categorized or tagged 
  - arbitrary markup

- Components
  - markup / css / script
  - api documentation / information

- Themes
  - has many asset manifests
  
- Pages
  - uniquely named
  - has many blocks

- Style Guides
  - has many pages
  - has one theme

### Component / Block Editor View 

The Editor View should be similar to JS Bin or Codepen.  It should allow
me to pull up a component and display the following:

```
                |
                | Slim / Jade / HTML 
                | 
  Live Preview  | -------
                | 
                | Sass / Less / CSS
                |
 -------------- | -------
                |
 Settings       | Coffeescript / Javascript 
                |
```
