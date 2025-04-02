---
title: HtmlSaveOptions.exportPageMargins property
linktitle: exportPageMargins property
articleTitle: exportPageMargins property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportPageMargins property. Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 210
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportPageMargins/
---

## HtmlSaveOptions.exportPageMargins property

Specifies whether page margins is exported to HTML, MHTML or EPUB.
Default is ``False``.



```js
get exportPageMargins(): boolean
```

### Remarks

Aspose.Words does not show area of page margins by default. 
If any elements are completely or partially clipped by the document edge the displayed area can be extended with
this option.


### Examples

Shows how to show out-of-bounds objects in output HTML documents.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Use a builder to insert a shape with no wrapping.
let shape = builder.insertShape(aw.Drawing.ShapeType.Cube, 200, 200);

shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.wrapType = aw.Drawing.WrapType.None;

// Negative shape position values may place the shape outside of page boundaries.
// If we export this to HTML, the shape will appear truncated.
shape.left = -150;

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to adjust the page to display out-of-bounds objects fully.
// If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
// If we set the "ExportPageMargins" flag to "false",
// our document will display the shape truncated as we would see it in Microsoft Word.
let options = new aw.Saving.HtmlSaveOptions();
options.exportPageMargins = exportPageMargins;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportPageMargins.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportPageMargins.html").toString();

if (exportPageMargins)
{
  expect(outDocContents.includes("<style type=\"text/css\">div.Section_1 { margin:72pt }</style>")).toEqual(true);
  expect(outDocContents.includes("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">")).toEqual(true);
}
else
{
  expect(outDocContents.includes("<style type=\"text/css\">")).toEqual(false);
  expect(outDocContents.includes("<div><p style=\"margin-top:0pt; margin-left:222pt; margin-bottom:0pt\">")).toEqual(true);
 }
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

