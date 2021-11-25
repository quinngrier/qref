# Qref

Qref is a JavaScript addon that adds selection permalinking to an HTML
page.

See
https://manuals.quinngrier.com/bash/4.1/bashref.html
for an example of Qref in action.
This is a copy of the Bash 4.1 manual with Qref added on.
When you select some text, a permalink popup will appear at the
beginning of the selection.
When you open the permalink, the selection will be highlighted and
scrolled into view.
This lets you create permalinks to arbitrary parts of the page.

Multiple selection permalinks can be created in browsers that natively
support multiple selection (e.g., using the Ctrl key in Firefox), or by
manually combining several permalinks.
To combine several permalinks, add all of the `qref=` parameters to the
same URL, separating them with `&` characters, or collapse them into a
single `qref=` parameter, separating the values with `+` characters.
For example, the following permalinks are equivalent:

* https://manuals.quinngrier.com/bash/4.1/bashref.html?qref=1-1.0.4&qref=1.0.15-2
* https://manuals.quinngrier.com/bash/4.1/bashref.html?qref=1-1.0.4+1.0.15-2

To add Qref to an HTML page, simply add it to the `<head>` element as
follows:

```
<script defer src="https://cdn.jsdelivr.net/npm/qref"></script>
```

You can also pin it to a specific version number:

```
<script defer src="https://cdn.jsdelivr.net/npm/qref@0.0.3"></script>
```

You can also download and serve it locally:

```
<script defer src="qref.js"></script>
```

Qref has no dependencies and does not make any web requests.
All you need is `qref.js`.
