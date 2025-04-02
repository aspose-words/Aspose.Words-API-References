---
title: HtmlSaveOptions.exportPageSetup property
linktitle: exportPageSetup property
articleTitle: exportPageSetup property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportPageSetup property. Specifies whether page setup is exported to HTML, MHTML or EPUB"
type: docs
weight: 220
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportPageSetup/
---

## HtmlSaveOptions.exportPageSetup property

Specifies whether page setup is exported to HTML, MHTML or EPUB.
Default is ``False``.



```js
get exportPageSetup(): boolean
```

### Remarks

Each [Section](../../../Aspose.Words/section/) in Aspose.Words document model provides page setup information
via [PageSetup](../../../Aspose.Words/pagesetup/) class. When you export a document to HTML format you might need to keep this information
for further usage. In particular, page setup might be important for rendering to paged media (printing)
or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature
is inactive by default.




### Examples

Shows how decide whether to preserve section structure/page setup information when saving to HTML.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");

let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.topMargin = 36.0;
pageSetup.bottomMargin = 36.0;
pageSetup.paperSize = aw.PaperSize.A5;

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to preserve or discard page setup settings.
// If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
// If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
// for the first section, and both sections will look identical.
let options = new aw.Saving.HtmlSaveOptions();
options.exportPageSetup = exportPageSetup;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportPageSetup.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportPageSetup.html").toString();

if (exportPageSetup)
{
  expect(outDocContents).toEqual(expect.stringContaining("@page Section_1"));
  expect(outDocContents).toEqual(expect.stringContaining("<div class=\"Section_1\">"));
}
else
{
  expect(outDocContents.includes("style type=\"text/css\">")).toEqual(false);
  expect(outDocContents.includes(
    "<div>" +
      "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Section 1</span>" +
      "</p>" +
    "</div>")).toBe(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

