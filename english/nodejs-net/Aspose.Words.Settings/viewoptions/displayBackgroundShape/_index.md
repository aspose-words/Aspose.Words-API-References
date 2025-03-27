---
title: ViewOptions.displayBackgroundShape property
linktitle: displayBackgroundShape property
articleTitle: displayBackgroundShape property
second_title: Aspose.Words for NodeJs
description: "ViewOptions.displayBackgroundShape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Settings/viewoptions/displayBackgroundShape/
---

## ViewOptions.displayBackgroundShape property

Controls display of the background shape in print layout view.


```js
get displayBackgroundShape(): boolean
```

### Examples

Shows how to hide/display document background images in view options.

```js
// Use an HTML string to create a new document with a flat background color.
const html = 
`<html>
  <body style='background-color: blue'>
    <p>Hello world!</p>
  </body>
</html>`;

let doc = new aw.Document(Buffer.from(html));

// The source for the document has a flat color background,
// the presence of which will set the "DisplayBackgroundShape" flag to "true".
expect(doc.viewOptions.displayBackgroundShape).toEqual(true);

// Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
// This may affect some text colors to improve visibility.
// Set the "DisplayBackgroundShape" to "false" to not display the background color.
doc.viewOptions.displayBackgroundShape = displayBackgroundShape;

doc.save(base.artifactsDir + "ViewOptions.displayBackgroundShape.docx");
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [ViewOptions](../)

