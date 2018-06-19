# Sticky Layout CSS
This repo is use to illustrate on the usage of sticky layout CSS without having to specify on the height of the sticky header or footer and having the content to be scrollable.

## Importing stylesheet
The main styling for the sticky layout CSS can be found in `sticky-layout.css`.
To use it, import the stylesheet into the header of the HTML. Refer to example below for importing it:

```html
<head>
  <!-- Rest of the tag(s) in the header... -->
  <link rel="stylesheet" href="sticky-layout.css">
</head>
```

## Usage
There are 4 CSS class names that compromises the usage of this sticky layout CSS.

```css
.sticky-layout { /* parent layout */ }
.sticky-layout__header { /* sticky header */ }
.sticky-layout__content { /* scrollable content */ }
.sticky-layout__footer { /* sticky footer */ }
```

`.sticky-layout` - _This class is the wrapper to the sticky layout and is dependent on the height of its relative element to display the content._

`.stick-layout__header` - _This class is the sticky header._

`.sticky-layout__content` - _This class is the content scrollable area. Any remaining spaces after being occupied by the header and the footer will be filled by the content layout._

`.sticky-layout__content` - _This class is the sticky footer._

## Example
Example usage of the class can be found in the `index.html` file. General usage would look something like below:

```html
<div style="height: 42vh;">
  <div class="sticky-layout">
    <div class="sticky-layout__header">
      <p>This is the header</p>
    </div>
    <div class="sticky-layout__content">
      <p>Scrollable content</p>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. In obcaecati reiciendis harum esse laboriosam, tempore at perspiciatis ducimus. Doloremque debitis quod inventore consectetur quae similique, aut commodi explicabo repellendus rerum?
      </p>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. In obcaecati reiciendis harum esse laboriosam, tempore at perspiciatis ducimus. Doloremque debitis quod inventore consectetur quae similique, aut commodi explicabo repellendus rerum?
      </p>
    </div>
    <div class="sticky-layout__footer">
      <p>This is the footer</p>
    </div>
  </div>
</div>
```

*NOTE*: Since the layout height and width is relatively dynamic, it is important to note that the height of the relative parent element for `.sticky-layout` be specified. This is due to the motivation of having the flexibility to define the content visibility.
