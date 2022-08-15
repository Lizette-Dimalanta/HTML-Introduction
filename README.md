# HTML Basics

Wednesday, 10 August 2022.

# Contents
1. __Notes__
2. __What is HTML?__
3. __Terminology__
4. __Absolute vs Relative__
5. __HTML Elements__
6. __Semantic Elements__
7. __HTML Forms__

# Notes:
- `git init` before `code .` in Ubuntu when making a new file.
- Live Server - can't connect? Try `localhost:[port #]` in URL.
- `[alt] + [click]`: Creates two cursors.
- Placeholder Images: [http://placekitten.com/300](http://placekitten.com/300)

## Emmet Snippets:
Syntax inspired by CSS selectors.
- `parent>child*[#]` __->__ `ul>li*3` (Creates list of `3` items.)
- `!` __->__ HTML Template
- `h1` __->__ `<h1></h1>`
- `lorem[# of words]` -> Placement Paragraph (Lorem Ipsum)
- `img` __->__ `<img src="link" alt="">`

__*Cheat Sheet*__: [Emmet.io - Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

# What is HTML?
- _HyperText Markup Language_ (HTML)
- Not a programming language (markup language)
- Tells browser how and where to display content on a webpage
- Must start with a declaration: `<!DOCTYPE html>`
- You can embed other content (videos, games, images etc.)
- __*Summary*__: HTML is the essential building block for webpages - you can add & mix in all sorts of other content, but you __must__ have HTML in there.

`HTML` merely presents data.

`CSS`: allows you to style HTML.

`JavaScript`: allows you to add interactivity & logic to your webpages.

__More Information:__ [W3Schools: HTML Basics](https://www.w3schools.com/html/html_basic.asp)

# Terminology
- ### __Algorithm__
    - A set of steps.

- ### __Meta Page Information__ _(Metadata)_
    `<meta charset="UTF-8">`
    - Gives additional information about a document.
    - Helps facilitate browser functionality.
        - Responsive Resizing
        - Locking in a text encoding strategy
    - __*Note*__: Having a meta tag implementing viewport information is crucial!

- ### __Character Set__ _(meta)_
    <meta charset=`"UTF-8"`>
        - Links CSS files.

- ### __Viewport__ _(meta)_
    `<meta name="viewport"content="width=device-width,initial-scale.0">`
        - Renders for mobile devices.

- ### __Link__ _(meta)_
    `<link rel="icon" type="image/x-icon" href="/path/to/some/favicon.ico">`
    - Can be used for a variety of things, such as:
        - Import JavaScript & CSS
        - Imports an imaginary image and sets it as the webpage's icon.

- ### __Comment__
    `<!--text-->`
    - Embeds comment into editor.
- ### __Tag__
    `<tag>`content`</tag>`
    - The way we markup our content.

- ### __Document Structure__
    `<!DOCTYPE html>`
    - Indicates version of html document.
    - Helps web browser process HTML files properly.

- ### __HTML__
    `<html></html>`
    - The _"container"_ for all other elements on the page (excluding `<!DOCTYPE html>`)

- ### __Head__
    `<head>`content`</head>`
    - Contains content that is __not__ shown on page
        - (Metadata, title, styling info.)
- ### __Body__
    `<body>`content`</body>`
    - Contains content that __is visible__ on the page.
    - Anything that is not contained in `<body></body>`, are not shown on the page.
- ### __Attributes__
    <img `src`="`alt`">
    - Aka. parameters on the command line.
    - Describes the properties of HTML elements.
- ### __Void Element__
    `<br>`

    `<img src="link" alt="description">`
    - Does not need closing tags.

- ### __Figure Element__
    `<Figure></Figure>`
    - Self-contained content, potentially with an option caption `<figcaption>` element.
    - Referred as a single element.
    ``` html
        <!DOCTYPE html>
        <html lang="en">
            <body>
                <figure>
                    <img src="link" alt="description">
                    <figcaption>Description - <a href="link">Source</a>
                    </figcaption>
                </figure>
            </body>
        </html>
    ```

# Absolute vs. Relative
## Absolute Path:
`<img src="https://placekitten.com/400/400">`
- Points to the complete path
- Usually begin with the web protocol (such as `https://`)
    - Link (internet)
    - Local file (complete path to root directory)

## Relative Path:
 `<img src="img/kitty.jpg">`
- Accessing a HTML file from a directory that is not the root directory.
- Typically begins with `"/"`
- Used to link different HTML pages.
- *with reference to current file.
```html
<!DOCTYPE html>
<head>
    <title>My Document</title>
</head>
<body>
    <h1 id="top">Heading 1</h1>
    <a href="#page-title">Link to another section on the same page</a>
    <a href="another_page">Link to another page</a>
    <!-- optional attributes are class and id -->
    <p class="red-text">Hello there!</p>
    <!-- id represents a unique value and can also be used to anchor to different section of the same page -->
    <h1 id="page-title">Home Page</h1>
    <a href="#top">Back to Top</a>
</body>
```

# HTML Elements

### __Some elements are...__
- __Inline:__ Runs on a single line.
- __Block:__ Runs over multiple lines.

- ### __Headings__

```html
    <h1></h1>
    <h2></h2>
    <h3></h3>
    <h4></h4>
    <h5></h5>
    <h6></h6>
```

- ### __Paragraph__
    `<p></p>`
    - A body of text.

- ### __Line Break__
    `<br></br>`
    - Separates line (from some HTML elements).

- ### __List__
    `<li></li>`: List item
    - Unordered List:
        ```html
        <ul>
            <li></li>
        </ul>
        ```
    - Ordered List:
        ```html
        <ol>
            <li></li>
        </ol>
        ```
    __*More Information*__: [HTML Lists on W3Schools](https://www.w3schools.com/html/html_lists.asp)

- ### __Table__
    `<table></table>`: Defines a table

    `<th></th>`: Header Cells

    `<tr></tr>`: Table Row

    `<td></td>`: Table Cells
    
    ``` html
    <table>
        <tr>
            <th>Person 1 (Tim)</th>
            <th>Person 2 (Tam)</th>
        <th>Person 3 (Tommy)</th>
        </tr>
        <tr>
            <td>Tim</td>
            <td>Tam</td>
            <td>Tommy</td>
        </tr>
        <tr>
            <td>2</td>
            <td>4</td>
            <td>6</td>
        </tr>
    </table>
    ```
__*More Information*__: [HTML Tables on W3Schools](https://www.w3schools.com/html/html_tables.asp)

- ### __Image__
    `<img src"link" alt="description"/>`
    - Self-closing tag.

    __*More Information*__: [HTML Images - W3Schools](https://www.w3schools.com/html/html_images.asp)

- ### __Anchor__ _(Hyperlink)_
    `<a href="link"/>[title]</a>`: Hyperlink Reference.

    `<a href="local.html"/>[title]</a>`: Relative Path.

    `<a href="#[id]"/>[title]</a>`: id -> anchors to different section of the same page.
    `<a href="file.html" target="_blank">[title]</a>`: Opens link in new tab (`target="_blank"`)

    __*More Information*__: [HTML Links - W3Schools](https://www.w3schools.com/html/html_links.asp)

- ### __Symbols__
    `<p>Text &#9829;</p>`

    __Currency Symbol List:__ [UTF-8 Currency Symbols - W3Schools](https://www.w3schools.com/charsets/ref_utf_currency.asp)

    __Arrow Symbol List:__ [UTF-8 Arrows - W3Schools](https://www.w3schools.com/charsets/ref_utf_arrows.asp)

    __Miscellaneous Symbol List:__ [UTF-8 Miscellaneous Symbols - W3Schools](https://www.w3schools.com/charsets/ref_utf_symbols.asp)


# Semantic Elements
- Semantic Elements = Elements with a meaning.
- An element of code that uses words to clearly represent what that element contains, in human language.

![Semantic Element](https://www.w3schools.com/html/img_sem_elements.gif)

__*Source*__: [W3Schools - HTML Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)

- `<article>`
    - Specifies independent, self-contained content.
    - Should make sense on its own, and it should be possible to distribute it independently from the rest of the website.
        - Forum Posts
        - Blog Posts
        - User Comments
        - Product Cards
        - Newspaper Articles
- `<aside>`
    - Defines content aside from the content it is placed in (like a sidebar).
    - Should be indirectly related to surrounding content.
- `<details>`
    - Defines additional details that the user can view or hide.
- `<figcaption>`
    - Defines a caption for `<figure>` element.
    - Can be placed as the first or last child of a `<figure>` element.
- `<figure>`
    - Specifies self-contained content.
        - Illustrations
        - Diagrams
        - Photos
        - Code Listings
        - etc.
- `<footer>`
    - Defines a footer for a document or section.
    - Typically contains:
        - Authorship Information
        - Copyright Information
        - Contact Information
        - Sitemap
        - Back to Top Links
        - Related Documents
    - __*Note*__: You can have several `<footer>` elements in one document.
- `<header>`
    - Represents a container for introductory content or a set of navigational links.
    - Typically contains:
        1. One or more heading elements (`<h1>` to `<h6>`)
        2. Logo or icon
        3. Authorship information
    - __*Note*__: You can have several `<header>` elements in one HTML document. However, `<header>` cannot be placed within a `<footer>`, `<address>` or another `<header>` element.
- `<main>`
    - Specifies the main content of a document.
- `<mark>`
- `<nav>`
    - Defines navigation links.
    ```html
    <nav>
        <a href="/html/">HTML</a>
        <a href="/css/">CSS</a>
        <a href="/js/">JavaScript</a>
        <a href="/jquery/">jQuery</a>
    </nav>
    ```
- `<section>`
    - Section in a document.
        ```html
        <section>
            <ul> 
                <li>Chapters</li>
                <li>Introduction</li>
                <li>News Items</li>
                <li>Contact Information</li>
        </section>
        ```
- `<summary>`
    - Defines a visible heading for a `<details>` element.
- `<time>`
    - Defines a date/time.

## Non-Semantic Elements:
- Tells nothing about its content (compared to semantic elements).
    - `<div>`
    - `<span>`

__*More Information*__: [HTML Semantic Elements - W3Schools](https://www.w3schools.com/html/html5_semantic_elements.asp)

# HTML Forms
- Forms are visual content which then needs to perform an action with the data entered by the user.
- Made up of multiple parts:
    1. __Form:__
        - The container for all other form-related elements.
        - Can be configured with an "action" property that tells the form to submit its data to a specific URL.
    2. __Input:__
        - The customisable, _depends-on-the-data-you-want_ element.
        - Can be configured to accept data in a variety of ways (such as fancy hidden password entries or time/date entries).
    3. __Label:__
        - Can be configured to correspond to input tags.
        - For some input tags (such as radio/checkbox buttons), it allows you to click on the label to select the input value.
        - Hugely useful for screenreader functionality.

__More Information:__ [W3Schools: HTML Forms](https://www.w3schools.com/html/html_forms.asp)
