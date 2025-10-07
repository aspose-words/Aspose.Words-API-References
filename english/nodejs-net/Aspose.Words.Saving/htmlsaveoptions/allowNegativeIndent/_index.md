---
title: HtmlSaveOptions.allowNegativeIndent property
linktitle: allowNegativeIndent property
articleTitle: allowNegativeIndent property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.allowNegativeIndent property. Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/allowNegativeIndent/
---

## HtmlSaveOptions.allowNegativeIndent property

Specifies whether negative left and right indents of paragraphs are normalized
when saving to HTML, MHTML or EPUB. Default value is ``false``.



```js
get allowNegativeIndent(): boolean
```

### Remarks

When negative indent is not allowed, it is exported as zero margin to HTML.
When negative indent is allowed, a paragraph might appear partially outside of the
browser window.




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

