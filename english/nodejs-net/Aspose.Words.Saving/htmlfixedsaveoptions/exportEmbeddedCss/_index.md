---
title: HtmlFixedSaveOptions.exportEmbeddedCss property
linktitle: exportEmbeddedCss property
articleTitle: exportEmbeddedCss property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.exportEmbeddedCss property. Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/exportEmbeddedCss/
---

## HtmlFixedSaveOptions.exportEmbeddedCss property

Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.


```js
get exportEmbeddedCss(): boolean
```

### Examples

Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// When we export a document to html, Aspose.words will also create a CSS stylesheet to format the document with.
// Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
// and link to the file from the html document using a <link> element.
// Setting the flag to "false" will embed the CSS stylesheet within the Html document,
// which will create only one file instead of two.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.exportEmbeddedCss = exportEmbeddedCss

const outPath = path.join(base.artifactsDir, "HtmlFixedSaveOptions.exportEmbeddedCss");
if (fs.existsSync(outPath))
  fs.rmSync(outPath, {recursive: true, force: true} );

doc.save(outPath + ".html", htmlFixedSaveOptions);
let outDocContents = fs.readFileSync(outPath + ".html").toString();

if (exportEmbeddedCss)
{
  expect(outDocContents.includes("<style type=\"text/css\">")).toBeTruthy();
  expect(fs.existsSync(path.join(outPath, "styles.css"))).toBeFalsy();
}
else
{
  expect(outDocContents.includes("<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions.exportEmbeddedCss/styles.css\" media=\"all\" />")).toBeTruthy();
  expect(fs.existsSync(path.join(outPath, "styles.css"))).toBeTruthy();
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

