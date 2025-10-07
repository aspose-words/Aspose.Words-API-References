---
title: HtmlSaveOptions.tableWidthOutputMode property
linktitle: tableWidthOutputMode property
articleTitle: tableWidthOutputMode property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.tableWidthOutputMode property. Controls how table, row and cell widths are exported to HTML, MHTML or EPUB"
type: docs
weight: 480
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/tableWidthOutputMode/
---

## HtmlSaveOptions.tableWidthOutputMode property

Controls how table, row and cell widths are exported to HTML, MHTML or EPUB.
Default value is [HtmlElementSizeOutputMode.All](../../htmlelementsizeoutputmode/#All).



```js
get tableWidthOutputMode(): Aspose.Words.Saving.HtmlElementSizeOutputMode
```

### Remarks

In the HTML format, table, row and cell elements
(**\<table\>**, **\<tr\>**, **\<th\>**, **\<td\>**)
can have their widths specified either in relative (percentage) or in absolute units.
In a document in Aspose.Words, tables, rows and cells can have their widths specified
using either relative or absolute units too.

When you convert a document to HTML using Aspose.Words, you might want to control how
table, row and cell widths are exported to affect how the resulting document is displayed
in the visual agent (e.g. a browser or viewer).

Use this property as a filter to specify what table widths values are exported into the destination document.
For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device,
then you probably want to avoid exporting absolute width values. To do this you need to specify
the output mode [HtmlElementSizeOutputMode.RelativeOnly](../../htmlelementsizeoutputmode/#RelativeOnly) or [HtmlElementSizeOutputMode.None](../../htmlelementsizeoutputmode/#None)
so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.




### Examples

Shows how to preserve negative indents in the output .html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a table with a negative indent, which will push it to the left past the left page boundary.
let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, Cell 1");
builder.insertCell();
builder.write("Row 1, Cell 2");
builder.endTable();
table.leftIndent = -36;
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(144);

builder.insertBreak(aw.BreakType.ParagraphBreak);

// Insert a table with a positive indent, which will push the table to the right.
table = builder.startTable();
builder.insertCell();
builder.write("Row 1, Cell 1");
builder.insertCell();
builder.write("Row 1, Cell 2");
builder.endTable();
table.leftIndent = 36;
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(144);

// When we save a document to HTML, Aspose.words will only preserve negative indents
// such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
// in a SaveOptions object that we will pass to "true".
let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.allowNegativeIndent = allowNegativeIndent;
options.tableWidthOutputMode = aw.Saving.HtmlElementSizeOutputMode.RelativeOnly;

doc.save(base.artifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.NegativeIndent.html").toString();

if (allowNegativeIndent)
{
  expect(outDocContents.includes(
    "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">")).toEqual(true);
  expect(outDocContents.includes(
    "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">")).toEqual(true); 
}
else
{
  expect(outDocContents.includes(
    "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">")).toEqual(true); 
  expect(outDocContents.includes(
    "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">")).toEqual(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

