---
title: HtmlSaveOptions.exportShapesAsSvg property
linktitle: exportShapesAsSvg property
articleTitle: exportShapesAsSvg property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportShapesAsSvg property. Controls whether [Shape](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3"
type: docs
weight: 250
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportShapesAsSvg/
---

## HtmlSaveOptions.exportShapesAsSvg property

Controls whether [Shape](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving
to HTML, MHTML, EPUB or AZW3.
Default value is ``false``.



```js
get exportShapesAsSvg(): boolean
```

### Remarks

If this option is set to ``true``, [Shape](../../../aspose.words.drawing/shape/) nodes are exported as \<svg\> elements.
Otherwise, they are rendered to bitmaps and are exported as \<img\> elements.





### Examples

Shows how to export shape as scalable vector graphics.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let textBox = builder.insertShape(aw.Drawing.ShapeType.TextBox, 100.0, 60.0);
builder.moveTo(textBox.firstParagraph);
builder.write("My text box");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation will export text box shapes.
// If we set the "ExportTextBoxAsSvg" flag to "true",
// the save operation will convert shapes with text into SVG objects.
// If we set the "ExportTextBoxAsSvg" flag to "false",
// the save operation will convert shapes with text into images.
let options = new aw.Saving.HtmlSaveOptions();
options.exportShapesAsSvg = exportShapesAsSvg;

doc.save(base.artifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.ExportTextBox.html").toString();

if (exportShapesAsSvg)
{
  expect(outDocContents.includes(
    "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
    "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">")).toBe(true);
}
else
{
  expect(outDocContents.includes(
    "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
      "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
      "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
    "</p>")).toBe(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

