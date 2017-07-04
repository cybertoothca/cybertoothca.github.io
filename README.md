# Cybertooth Ember Addons Cheat Sheet

## [ember-cli-bootstrap3-carousel](http://ember-cli-bootstrap3-carousel.cybertooth.io)

### `twbs-carousel` Component ([ :octocat: docs](https://github.com/cybertoothca/ember-cli-bootstrap3-carousel#components))

```hbs
{% raw %}
{{#twbs-carousel as |carousel|}}
  {{#carousel.slide classNames="active" as |slide|}}
    {{slide.img src="https://dummyimage.com/1600x900/f7d3a0/333.jpg&text=Slide+1" alt="A slide image."}}
  {{/carousel.slide}}
  {{#carousel.slide as |slide|}}
    {{slide.img lazy="https://dummyimage.com/1600x900/f7d3a0/333.jpg&text=Slide+2" alt="A slide image."}}
  {{/carousel.slide}}
  ...
  {{#carousel.slide as |slide|}}
    {{slide.img lazy="https://dummyimage.com/1600x900/f7d3a0/333.jpg&text=Slide+5" alt="A slide image."}}
  {{/carousel.slide}}
{{/twbs-carousel}}
{% endraw %}
```

## [ember-cli-bootstrap3-forms](http://ember-data-bootstrap3-forms.cybertooth.io/)

### `twbs-errors-alert` Component ([:octocat: docs](https://github.com/cybertoothca/ember-data-bootstrap3-forms#twbs-errors-alert))

```hbs
{% raw %}
{{twbs-errors-alert class="alert-danger" model=model}}
{% endraw %}
```

### `twbs-form-group` Component ([:octocat: docs](https://github.com/cybertoothca/ember-data-bootstrap3-forms#twbs-form-group))

```hbs
{% raw %}
{{#twbs-form-group fieldErrors=model.errors.firstName}}
  <label for="...">...</label>
  {{input class="form-control" id="..." type="..." value=model.firstName}}
  <p class="help-block">...</p>
{{/twbs-form-group}}
{% endraw %}
```

## [ember-cli-bootstrap3-grid](https://github.com/cybertoothca/ember-cli-bootstrap3-grid)

### `twbs-clearfix` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-bootstrap3-grid/blob/master/README.md#twbs-clearfix))

```hbs
{% raw %}
{{twbs-clearfix columnCount=3 index=index visible-sm=true visible-md=true visible-lg=true}}
{% endraw %}
```

```hbs
{% raw %}
{{twbs-clearfix columnCount=3 index=index visible-all=true}}
{% endraw %}
```

### `Viewport` Mixin ([:octocat: docs](https://github.com/cybertoothca/ember-cli-bootstrap3-grid/blob/master/README.md#viewport))

```js
import Viewport from 'ember-cli-bootstrap3-grid/mixins/viewport';
// ... then mix it into your component
export default Ember.Component.extend(Viewport, { ... });
```

```hbs
{% raw %}
{{!-- then in your template use the computed functions --}}
{{#if xs?}} Extra Small {{else}} SM/MD/LG {{/if}}
{% endraw %}
```

## [ember-cli-bootstrap3-popover](http://ember-cli-bootstrap3-popover.cybertooth.io)

### `twbs-popover` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-bootstrap3-popover#twbs-popover))

```hbs
{% raw %}
{{#twbs-popover content="Click again to hide." as |popover|}}
  {{#popover.trigger}}
    <a href="javascript:void(0)">Click this anchor.</a>
  {{/popover.trigger}}
{{/twbs-popover}}
{% endraw %}
```

## [ember-cli-date-textbox](http://ember-cli-date-textbox.cybertooth.io)

### `input-date` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-date-textbox#input-date))

```hbs
{% raw %}
{{input-date autofocus=true classNames="form-control" date=model.createdAt displayFormat="LLLL"}}
{% endraw %}
```

### `input-iso8601` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-date-textbox#input-iso8601))

```hbs
{% raw %}
{{input-iso8601 classNames="form-control" displayFormat="llll" iso8601="2017-07-01T00:00:00.000Z"}}
{% endraw %}
```

## [ember-cli-marked-down](https://github.com/cybertoothca/ember-cli-marked-down)

### `marked-down` Helper ([:octocat: docs](https://github.com/cybertoothca/ember-cli-marked-down#marked-down-some-__markdown__-text))

```hbs
{% raw %}
{{marked-down "Some ~~struck~~ markdown text" strikethrough=true}}
{% endraw %}
```

### `set-links-target` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-marked-down#set-links-target))

```hbs
{% raw %}
{{#set-links-target excludeSelfLinks?=true targetValue="_blank"}}
  ...
{{/set-links-target}}
{% endraw %}
```

## [ember-cli-text-support-mixins](http://ember-cli-text-support-mixins.cybertooth.io)

### `input-text` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-text-support-mixins#input-text))

```hbs
{% raw %}
{{input-text autofocus=true class="form-control" escapeKeyClears?=true focusSelectsText?=true value=model.firstName}}
{% endraw %}
```

### `text-area` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-text-support-mixins#text-area))

```hbs
{% raw %}
{{text-area class="form-control" escapeKeyClears?=true focusSelectsText?=true ctrlEnterSubmitsForm?=true value=model.notes}}
{% endraw %}
```

## [ember-cli-textarea-autosize](http://ember-cli-textarea-autosize.cybertooth.io)

### `textarea-autosize` Component ([:octocat: docs](https://github.com/cybertoothca/ember-cli-textarea-autosize#usage))

```hbs
{% raw %}
{{textarea-autosize classNames="form-control" rows=4}}
{% endraw %}
```
