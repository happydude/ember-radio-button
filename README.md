# ember-radio-button [![Build Status](https://travis-ci.org/yapplabs/ember-radio-button.svg?branch=master)](https://travis-ci.org/yapplabs/ember-radio-button) [![Ember Observer Score](https://emberobserver.com/badges/ember-radio-button.svg)](https://emberobserver.com/addons/ember-radio-button)

**Note**: **ember-radio-button 1.0.0 requires using htmlbars**.  For applications not using htmlbars, use version 0.1.3 or the `pre-htmlbars`
 branch

This ember-cli addon provides a `radio-button` component.

Pass two properties to the component: `value` and `groupValue`.  A `radio-button`
 will be in a checked state when `groupValue === value`.

Clicking on a `radio-button` will set `groupValue` to its `value`.

The component exposes a `changed` action that allows you to do something
when a user interaction causes one of your radio buttons to update `groupValue`.

**Template:**
```javascript
{{radio-button
    value="green"
    groupValue=color
    changed="colorChanged"}}

{{#radio-button
    value="blue"
    groupValue=color
    changed="colorChanged"}}
    Blue
{{/radio-button}}
```

**Results in:**
```html
<input id="ember345" class="ember-view" type="radio" value="green">

<label id="ember346" class="ember-view ember-radio-button">
  <input id="ember347" class="ember-view" type="radio" value="blue">
  Blue
</label>
```

You can additionally provide `disabled` `name` and `required` properties to a `radio-button`

```javascript
{{radio-button
    value="green"
    groupValue=color
    required=true
    disabled=true
    name="color"}}
```

```html
<input id="ember345" class="ember-view" type="radio" value="green" name="color" required disabled>
```

The `radioId` and `radioClass` properties allow specifying the id and adding classnames to the input tag.  When radioId is specified, the label tag's `for` attribute will also use it.

```javascript
{{#radio-button
    radioId="purple-radio"
    radioClass="my-custom-class"
    value="purple"
    groupValue=color
    changed="colorChanged"}}
    Purple
{{/radio-button}}
```

```html
<label id="ember346" for="purple-radio" class="ember-view ember-radio-button">
  <input id="purple-radio" class="ember-view my-custom-class" type="radio" value="purple">
  Purple
</label>
```

## Installing

ember-cli 0.2.3+

`ember install ember-radio-button`

older ember-cli versions

`ember install:npm ember-radio-button`

## Collaborating on this repo

* `git clone <repository-url>` this repository
* `cd ember-radio-button`
* `npm install`

## Running

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).

## Running Tests

* `npm test` (Runs `ember try:each` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`

## Building

* `ember build`

For more information on using ember-cli, visit [https://ember-cli.com/](https://ember-cli.com/).
