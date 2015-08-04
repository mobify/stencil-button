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

During installation, AdaptiveJS will register a Dust helper for the component which can be used in any template.



### With options from data

Assuming a context of the form:

```javascript
var context = {
    myButtonData: {
        id: 'something',
};
```

```html
{#myButtonData}
    {@c-button id=id}Some Text{/c-button}
{/myButtonData}
```



## API

### Dust helper parameters

Param name | Type          | Description
:--------- | :------------ | :----------
class      | String        | Adds values to the `class` attribute of the root element
id         | String        | Sets the `id` attribute of the root element
link       | String        | Creates anchor button with link specified
type       | String        | Specifies button type
disabled   | Boolean       | True if you would like button to be disabled (default:false)


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