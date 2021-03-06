# t7/accordion

Create an 'accordion' style React component from a single structure

This component functions similarly to `<AccordionMulti/>` except that it only allows for one area to be expanded at a time.

By default accordion areas are collapsed. To render an area open, pass an object with the corresponding index set to `true`.


## Installation
```sh
npm install @t7/accordion --save
```

## Usage
```js
import Accordion, { AccordionPanel } from '@t7/accordion'
import '@t7/accordion/dist/index.css'
```
```js
/* indicate the selected item */
let selected = {
  0: true
}

/* create a "handler" if your appliction requires additional processing when tabs are selected */
const handleClick = (e, index, label, selected) => {
  <do something interesting>

  /*
    `e` is the event.

    `index` is the numeric position.

    `label` is the text itself.

    `selected` is the state object.
  */
}

.
.
.

/* create your accordion as a single logical grouping */
<Accordion selected={selected} handleClick={handleClick}>
  <AccordionPanel label='Item 1'>
    <p>
      Content for "Item 1"
    </p>
  </AccordionPanel>
  <AccordionPanel label='Item 2'>
    <p>
      Content for "Item 2"
    </p>
  </AccordionPanel>
  <AccordionPanel label='Item 3'>
    <p>
      Content for "Item 3"
    </p>
  </AccordionPanel>
</Accordion>

```
&nbsp;
&nbsp;

### Note regarding the use of the _required_ CSS
_*if your build process will not resolve the CSS in a module copy the file `@t7/accordion/dist/index.css` from the node_modules folder and reference the copy with an HTML link *_  
  
```xml
e.g.
<link rel="stylesheet" type="text/css" href="<your stylesheet folder>/@t7/accordion/dist/index.css">
```
