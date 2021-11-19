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

* https://manuals.quinngrier.com/bash/4.1/bashref.html?qref=1.0.0-1.0.4&qref=1.0.15-1.0.21
* https://manuals.quinngrier.com/bash/4.1/bashref.html?qref=1.0.0-1.0.4+1.0.15-1.0.21

To add Qref to an HTML page, simply include it in the `<head>` element
as follows:

```
<script defer src="qref.js"></script>
```
