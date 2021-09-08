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
    - Anchor: `a` (a link to somewhere else) \
        ```
        <a href="link">Text</a>
        ```
    - Division: `div` (cardboard box)
    - Span: `span` (ziploc bag, a container for small pieces of text)
    - List: `ol` & `ul` (ordered & unordered), li (item insise the list)
    - Button: `button` 
    - Image: `img` \
        ```
        <img src="location" alt="descriptive content"/>
        ```
        - content: `img` tag```
        - background/decorative: css
    - Browser input: `input`
        - default: text
    - More text: `textarea`
        - not self closing
    - Dropdown menu: `select` & `option`\
        ```
        <select><option value="option1">option1</option><option value="option2">option2</option></select>
        ```
        - `value`: send back to the server
    - Group tags: `form` (a container for data from a user input)
    - Tables: `table`, `tr` (one row), `td` (one cell) \
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
- 
    ```
    <!-- this is a comment-->
    ```
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
- `.<class name>` or `tag`
- Always style on classes, don't style on tags
- In CSS, when two rules points to the same class
    - The one that comes the last wins
    - Property by property
    - The more specific one wins
        - e.g. `.main-brand-3.title-3`
    - **Class > tags:** classes are more specific than tags
