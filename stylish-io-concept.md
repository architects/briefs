# Concept Notes: Stylish 

Stylish is a tool for creating / cloning / editing component style guides in the context
of one or more themes.

A component style guide is a presentation of multiple components on a single page,
along with information about them, their API, example code, etc.  The
component style guide will share a common visual aesthetic or theme.

A component is made up of markup, javascript, and css.  I intend to be
able to export the components as standard web components / custom
elements, or polymer custom elements.

## Marketing Site / Splash Page

I have the stylish.io domain, and intend to make the stylish editor capable of publishing themes / components to the stylish.io site, and potentialy develop a marketplace for them.


## Inspirations

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

### Designmodo Startup Framework

The Designmodo startup framework is a collection of 'Blocks'. A Block is
a root level HTML element nested directly under the body tag, or in some
cases, a container element which is the only descendant of the body tag.

A block may contain zero or more components. 

The startup framework divides up their package into categories of
blocks:

- headers
- footers
- content
- contacts
- prices
- projects
- crews

This allows you to mix and match blocks to build page layouts. You can
use http://designmodo.com/generator to see how this is used.  

When you export something from the generator, it will give you the
markup for the blocks, as well as the css / less for that block. It will
wrap all of this up in a general HTML page which includes the global /
common / shared dependencies.

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
