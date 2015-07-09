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

### With a pre-existing select element

```html
{@c-button element=selectMarkupOrElement /}
```


### With options from data

Assuming a context of the form:

```javascript
var context = {
    myButtonData: {
        id: 'something',
        buttonText: 'something',
};
```

```html
{#myButtonData}
    {@c-button id=id buttonText=buttonText/}
{/myButtonData}
```



## API

### Dust helper parameters

Param name | Type          | Description
:--------- | :------------ | :----------
class      | String        | Adds values to the `class` attribute of the root element
id         | String        | Sets the `id` attribute of the root element
element    | DOM, String   | Accepts the underlying button element as a DOM node or HTML string
text       | String        | Creates Button Text
buttonType | String        | Creates predefined button styles. One of `basic`, `success` or `error`
isSecondary| Boolean       | true if you would like a secondary button (default:false)
customClass| String        | Add a custom class to your button
textAlign  | String        | Sets text align of button text. One of `left`, `right` or `center` (default:center)
size       | String        | sets size of button. One of `large`, `xlarge` or `xxlarge`


### Sass configurable variables

Variable name             | Type      | Description
:------------------------ | :-------- | :----------
$border-width-button      | String    | Sets border width of all buttons (ex `2px`)
$border-style-button      | String    | Sets style of border
$border-radius-button     | String    | Sets border radius of all buttons (ex `2px`)
$basic-button             | String    | sets colour of basic button (ex `#cccccc`)
$active-basic-button      | String    | sets colour of basic button when active (ex `#cccccc` )
$disabled-basic-button    | String    | sets colour of basic button when disabled (ex `#cccccc)
$success-button           | String    | sets colour of success button
$active-success-button    | String    | sets colour of success button when active (ex `#cccccc` )
$disabled-success-button  | String    | sets colour of success button when disabled (ex `#cccccc`)
$error-button             | String    | sets colour of error button
$active-error-button      | String    | sets colour of error button when active (ex `#cccccc` )
$disabled-error-button    | String    | sets colour of error button when disabled (ex `#cccccc`)
$large-button             | String    | sets size of large button (ex `20px`)
$padding-large-button     | String    | sets padding of large button (ex `20px 20px`)
$xlarge-button            | String    | sets size of xlarge button (ex `20px`)
$padding-xlarge-button    | String    | sets padding of xlarge button (ex `20px 20px`)
$xxlarge-button           | String    | sets size of xxlarge button (ex `20px`)
$padding-xxlarge-button   | String    | sets padding of xxlarge button (ex `20px 20px`)


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