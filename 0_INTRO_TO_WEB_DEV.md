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
### Coments
- 
    ```
    <!-- this is a comment-->
    ```