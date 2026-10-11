# Search

A front-end recreation of Google's Search, Image Search, and Advanced Search pages built as part of Harvard's CS50 Web Programming with Python and JavaScript.

## Features

* Google Search page
* Google Image Search page
* Google Advanced Search page
* "I'm Feeling Lucky" button support
* Pure HTML and CSS implementation

## Structure

```bash
cs50w-search
├── index.html
├── images.html
├── advanced.html
├── assets
│   └── wc-doodle-2026.gif
├── README.md
└── style.css
```

## Pages

### Search

Allows users to perform a standard Google search using the `q` query parameter.

### Image Search

Redirects users to Google Images search results using:

```text
q=<query>
```

and the image search parameter:

```text
tbm=isch
```

### Advanced Search

Supports Google's advanced search parameters:

| Field               | Parameter |
| ------------------- | --------- |
| All these words     | `as_q`    |
| Exact phrase        | `as_epq`  |
| Any of these words  | `as_oq`   |
| None of these words | `as_eq`   |

### I'm Feeling Lucky

Uses Google's `btnI` parameter to open the first search result directly.

Note: Google may display a redirect notice before navigating to the destination website. This is expected behavior.

## Technical Notes

This project intentionally relies on HTML forms and URL query parameters instead of JavaScript.

The goal is to understand how search forms communicate with web servers through HTTP GET requests.

Examples:

```text
https://www.google.com/search?q=harvard+cs50
```

```text
https://www.google.com/search?q=cat&tbm=isch
```

```text
https://www.google.com/search?as_q=harvard+cs50&as_epq=web+programming
```

## Running Locally

Clone the repository:

```bash
git clone https://github.com/bassam-alaraby/cs50w-search.git
cd cs50w-search
```

Open `index.html` directly in a browser.

Or serve the project using a local development server:

```bash
python -m http.server
```

Then visit:

```text
http://localhost:8000
```

## Technologies

* HTML5
* CSS3
* Google Search GET Parameters
