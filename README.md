# Stencil Button

A styleable, accessible `<button>` component for [Mobify’s AdaptiveJS framework](http://adaptivejs.mobify.com/).

**View demo (coming soon)**


## Requirements

- AdaptiveJS 2.1 or greater


## Installation

```shell
cd my/adaptive/project
grunt component:install:button
```


## Usage

During installation, AdaptiveJS will register a Dust helper for the component which can be used in any template. The most common usage is shown below:

```html
{! Renders as a `<button class="c-button" type="button">...`. !}
{@c-button}Label{/c-button}

{! Renders as a `<button class="c-button" type="submit">...` !}
{@c-button type="submit"}Label{/c-button}

{! Renders as a `<a class="c-button" href="foo/bar">...` !}
{@c-button href="foo/bar"}Label{/c-button}
```


## API

### Dust helper parameters

Param name | Type            | Description
:--------- | :-------------- | :----------
class      | String          | Adds values to the `class` attribute of the root element
id         | String          | Sets the `id` attribute of the root element
href       | String          | If specified, the component is rendered as a link, with this value set as the href
type       | button|submit   | Specifies button type. Defaults to `button`, which is different from the default for HTML.
disabled   | Boolean         | Pass "true" if you would like button to be disabled

### Dust helper bodies

Body name | Accepts        | Description
:-------- | :------------- | :----------
body      | Any element(s) | Accepts any HTML elements. Typically a text label, but may include other elements such as an Icon.

### Sass configurable variables

_none_

### UI options, methods and events

_none_ (Button has no UI script.)


## Contributing

First, read the Adaptive component documentation, especially the pages on creating components and the Stencil authoring guide. Then, clone the repo:

- `git clone git@github.com:mobify/stencil-button.git`
- `cd stencil-button`
- `npm install && bower install`
- Create a branch for your changes and begin development.
- Run the test server during development to check your work (see below).

### Testing

Visual tests provide a way to describe the features of a component in a spec format and manually check functionality of a component. To run tests:

- `grunt serve`
- Note the local port on which the test server is running (defaults to 3000)
- Navigate to [localhost:{port}/tests/visual](http://localhost:3000/tests/visual)
