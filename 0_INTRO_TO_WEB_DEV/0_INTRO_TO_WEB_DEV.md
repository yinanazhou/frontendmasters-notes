# Complete Intro to Web Development
## Introduction
- Notes link: https://btholt.github.io/intro-to-web-dev-v2/
- HTML is the structure.
- CSS is the blueprint.
- JaveScript is the smart home.
- Web Dev Tools:
    - MDN: https://developer.mozilla.org/en-US/
    - CSS-Tricks: https://css-tricks.com/ \
        Flexbox: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

## Learning HTML
- Static
### Tag
- Base building block
- Types of Tags
    - Headings: `h1` - `h6`
    - Paragraph: `p` (only text goes in p tags)
    - Anchor: `a` (a link to somewhere else)
        ```
        <a href="link">Text</a>
        ```
    - Division: `div` (cardboard box)
    - Span: `span` (ziploc bag, a container for small pieces of text)
    - List: `ol` & `ul` (ordered & unordered), li (item inside the list)
    - Button: `button` 
    - Image: `img`
        ```
        <img src="location" alt="descriptive content"/>
        ```
        - content: `img` tag
        - background/decorative: css
    - Browser input: `input`
        - default: text
    - More text: `textarea`
        - not self closing
    - Dropdown menu: `select` & `option`
        ```
        <select><option value="option1">option1</option><option value="option2">option2</option></select>
        ```
        - `value`: send back to the server
    - Group tags: `form` (a container for data from a user input)
    - Tables: `table`, `tr` (one row), `td` (one cell)
        ```
        <table>
            <tr>
                <td>(0,0)</td>
                <td>(1,0)</td>
            </tr>
            <tr>
                <td>(0,1)</td>
                <td>(1,1)</td>
            </tr>
        </table>
        ```
        <table><tr><td>(0,0)</td><td>(1,0)</td></tr><tr><td>(0,1)</td><td>(1,1)</td></tr></table>
    - Bold: `strong`
    - Italic: `em`
### Comments
`<!-- this is a comment-->`
### HTML Attributes
### HTML Class
- Classes are special attributes that can go on any tag
- Go with CSS and JavaScript
- Can have multiple classes \
`class="post featured-post"`
### HTML IDs
- ID need to be unique, the only one on the page
- IDs are useful for linking, deep link directly to that point in the page
### Naming and Semantics
- Name things after what it does, not what it looks like
- HTML: kebab case; CSS: camel case
### Meta HTML
- Boilerplate
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>My amazing HTML Document</title>
    </head>
    <body>
        <h1>Check this out</h1>
        <!-- Your amazing HTML here -->
    </body>
    </html>
    ```
- `<script></script>`, `<style></style>`, and `<link />`
    - `<script></script>` links JavaScript into HTML
    - `<style></style>` and `<link />` bring in CSS

## Learning CSS
### Introducing CSS
- rules
- 
    ```
    h1 {
        color: limegreen;
        font-size: 60px;
        font-weight: normal;
        text-decoration: underline;
        text-transform: uppercase;
        border: 3px solid pink;
    }
    ```
    - `h1` -> the selector
    - `color` -> property
    - `limegreen` -> value
    - `font-weight` -> bold/normal/light
    - `text-decoration` -> underline/line-through/overline
    - `text-transform` -> uppercase/lowercase/capitalize
### Parents & Children
### CSS Playground
- Codepen: https://codepen.io/btholt/pen/ELaxOB
### CSS Selectors & Cascade
- `.<class name>` or `tag` or `#<ID name>`
- Always style on classes, don't style on tags
- In CSS, when two rules points to the same class
    - The one that comes the last wins
    - Property by property
    - The more specific one wins
        - e.g. `.main-brand-3.title-3`
    - **Class > tags:** classes are more specific than tags
### IDs
- `!important` > ID > Class + tag
### Comment in CSS
`/* anything between this is a comment */`
### Pseudoclasses
- ```
    <style>
      .hover-example {
        width: 100px;
        height: 100px;
        background-color: limegreen;
        color: white;
      }
      .hover-example:hover { \\ this is pseudoclass
        background-color: crimson;
        width: 150px;
        height: 150px;
      }
    </style>
    <div class="hover-example">Hover your mouse over me</div>
    ```
- Specificity == class
- In list:
    - first-child
    - nth-child(2)
    - nth-child(2n + 1) -> odd numbers
    - last-child
### Pseudoelements
### Wildcard Selector
- `*`: everything
### CSS Specificity Guide
- CSS SpeciFISHity guide: http://www.standardista.com/css3/css-specificity/
### CSS Box Model
#### Display
- div -> display: block
- span -> display: inline
- inline-block
- flex & inline-flex
- grid & inline-grid
- table: use table in html instead
#### Height, Width, Padding, Border, and Margin
- Order: interior content -> padding -> border -> margin
- Trick: for every website
    ```buildoutcfg
    * {
        box-sizing: border-box; // make box size include border
    }
### CSS Floats & Flexbox
- ```
  .floated .box{ //all the box inside floated
    float: left;
  }
  ```
- float: cannot go higher than the previous box
- flex: works on the parent container
    - ```
        <style>
          .jc-center {
            justify-content: flex-end; //everything to the right as far as possible
          }
        </style>
      ```
    - by default, no wrap
    - `justify-content`
        <table>
            <tr>
                <td>`justify-content: flex-start`</td>
                <td>everything to the left (default)</td>
            </tr>
            <tr>
                <td>`justify-content: flex-end`</td>
                <td>everything to the right</td>
            </tr>
            <tr>
                <td>`justify-content: center`</td>
                <td>everything to the middle</td>
            </tr>
            <tr>
                <td>`justify-content: space-between`</td>
                <td>evenly spaced (no space at beginning and end)</td>
            </tr>
            <tr>
                <td>`justify-content: space-around`</td>
                <td>space: half, one, half</td>
            </tr>
            <tr>
                <td>`justify-content: space-evenly`</td>
                <td>evenly spaced (space at beginning and end</td>
            </tr>
        </table>
    - `align-items`
        <table>
            <tr>
                <td>`align-items: flex-start`</td>
                <td>everything to the top (default)</td>
            </tr>
            <tr>
                <td>`align-items: flex-end`</td>
                <td>everything to the bottom</td>
            </tr>
            <tr>
                <td>`align-items: center`</td>
                <td>everything to the vertical middle</td>
            </tr>
            <tr>
                <td>`align-items: stretch`</td>
                <td>stretch the box to the assigned `height` or the highest height</td>
            </tr>
        </table>
### Effective Patterns for Writing CSS
#### Connecting CSS and HTML
- in `index.html`
  ```
    <html lang="en">
    <head>
      <title>My amazing HTML Document</title>
      <link rel="stylesheet" href="./style.css" />
    </head>
    <body>
      <h1 class="my-brand">Check this out</h1>
      <!-- Your amazing HTML here -->
    </body>
    </html>
  ```
#### When to Actually Use the Cascade
- when share most of the styles, cascade for small details

## Learning JavaScript
### Programming Fundamentals
- `const` indicates **unchanging** value
### Numbers, Strings, and Booleans
- String
    - Single quote, double quote, or back tick
    - Strings can be concatenated using `+`
    - Template string: 
        - Use bakctick
        - e.g. ``const sentenceWithTemplate = `Hello ${firstName} ${lastName}! How are you?\` ``
    
- Comments
    - `// this is a comment`
    - `/* this is a comment */`
    
- Booleans: `true` or `false`
- Numbers: only one type of number in JS
### Control Flow
- ```
  if (condition) {
  statement;
  } else {
  statement;
  }``` 
- always use `===`, `==` can compare string with number
- `!==` is not equal to
### Loops
- `let` indicates **changing** values
- while loop:
  ```
  let friends = 0;
  with (friends < 10) {
  friends = friends + 1;
  }
  ```
- for loop:
  ```
  let friends = 0;
  for (let i = 0; i <= 10; i++) {
  friends = friends + 1;
  }
  ```
### Functions
### Scope
- reference error
### Builtins
- String
    - .toLowerCase()
    - .toUpperCase()
    - .substr(start_index, number_of_characeter)
- Math.
### Objects & Arrays

