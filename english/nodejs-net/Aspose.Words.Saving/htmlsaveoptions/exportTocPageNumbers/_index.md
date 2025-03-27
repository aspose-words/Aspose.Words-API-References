---
title: HtmlSaveOptions.exportTocPageNumbers property
linktitle: exportTocPageNumbers property
articleTitle: exportTocPageNumbers property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportTocPageNumbers property. Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB"
type: docs
weight: 270
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportTocPageNumbers/
---

## HtmlSaveOptions.exportTocPageNumbers property

Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB.
Default value is ``False``.



```js
get exportTocPageNumbers(): boolean
```

### Examples

Shows how to display page numbers when saving a document with a table of contents to .html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
// style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
// and the page number that contains the heading on the right.
let fieldToc = builder.insertField(aw.Fields.FieldType.FieldTOC, true).asFieldToc();

builder.paragraphFormat.style = builder.document.styles.at("Heading 1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Entry 1");
builder.writeln("Entry 2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Entry 3");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Entry 4");
fieldToc.updatePageNumbers();
doc.updateFields();

// HTML documents do not have pages. If we save this document to HTML,
// the page numbers that our TOC displays will have no meaning.
// When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
// If we set the "ExportTocPageNumbers" flag to "true",
// each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
// If we set the "ExportTocPageNumbers" flag to "false",
// the save operation will omit both the separator and page number and leave the heading for each entry intact.
let options = new aw.Saving.HtmlSaveOptions();
options.exportTocPageNumbers = exportTocPageNumbers;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportTocPageNumbers.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportTocPageNumbers.html").toString();

if (exportTocPageNumbers)
{
  expect(outDocContents.includes(
                "<span>Entry 1</span>" +
                "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
                "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
                "<span>2</span>" +
                "</p>")).toEqual(true);
}
else
{
  expect(outDocContents.includes(
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Entry 2</span>" +
                "</p>")).toEqual(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

