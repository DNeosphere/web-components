# Web Components

## Basic principles

### Custom Elements

How to define them:

```js
class MyTag extends HTMLElement {...}

// This binds the custom element to the DOM
window.customElements.define('my-tag', MyTag)
```

How to use them:

```html
<my-tag>Hello World</my-tag>
```

> > > The custom elements will have the LifeCycle methods available

- _constructor()_ called when an instance of the element is created or upgraded useful to intialize any state or event listeners

- connectedCallback(): Called everytime the element is inserted into the DOM

- disconnectedCallback(): Called everytime the element is removed from the DOM

- attributeChangedCallback(atrrName, oldValue, newValue): Called when an attribute suffers any change. Similar behaviour like props in React

### Shadow DOM

- Used for self-contained components
- Encapsulates styles and markup, meaning these won't affect the regular DOM
- Creates a shadowRoot that we can reference and interact with

usage:

```js
// Open mode allows the element to be inspected with the browser's devTools
element.attachShadow({ mode: open });
```

### HTML Templates

- Define the encaptsulated markup of our web components
- Tempalte tags stores markup on page
- Include both HTML and CSS in templates
- Use slots to add custom text
