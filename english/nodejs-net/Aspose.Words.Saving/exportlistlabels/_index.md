---
title: ExportListLabels enumeration
linktitle: ExportListLabels enumeration
articleTitle: ExportListLabels enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ExportListLabels enumeration. Specifies how list labels are exported to HTML, MHTML and EPUB."
type: docs
weight: 180
url: /nodejs-net/aspose.words.saving/exportlistlabels/
---

## ExportListLabels enumeration

Specifies how list labels are exported to HTML, MHTML and EPUB.


### Members

| Name | Description |
| --- | --- |
| Auto | Outputs list labels in auto mode. Uses HTML native elements when possible. |
| AsInlineText | Outputs all list labels as inline text. |
| ByHtmlTags | Outputs all list labels as HTML native elements. |

### Examples

Shows how to configure list exporting to HTML.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);
builder.listFormat.list = list;

builder.writeln("Default numbered list item 1.");
builder.writeln("Default numbered list item 2.");
builder.listFormat.listIndent();
builder.writeln("Default numbered list item 3.");
builder.listFormat.removeNumbers();

list = doc.lists.add(aw.Lists.ListTemplate.OutlineHeadingsLegal);
builder.listFormat.list = list;

builder.writeln("Outline legal heading list item 1.");
builder.writeln("Outline legal heading list item 2.");
builder.listFormat.listIndent();
builder.writeln("Outline legal heading list item 3.");
builder.listFormat.listIndent();
builder.writeln("Outline legal heading list item 4.");
builder.listFormat.listIndent();
builder.writeln("Outline legal heading list item 5.");
builder.listFormat.removeNumbers();

// When saving the document to HTML, we can pass a SaveOptions object
// to decide which HTML elements the document will use to represent lists.
// Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
// will create lists by formatting spans.
// Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the <p> tag
// to build lists in cases when using the <ol> and <li> tags may cause loss of formatting.
// Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
// will use <ol> and <li> tags to build all lists.
let options = new aw.Saving.HtmlSaveOptions();
options.exportListLabels = exportListLabels;

doc.save(base.artifactsDir + "HtmlSaveOptions.list.html", options);
let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.list.html").toString();

switch (exportListLabels)
{
  case aw.Saving.ExportListLabels.AsInlineText:
    expect(outDocContents.includes(
      "<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">" +
        "<span style=\"-aw-import:ignore\">" +
          "<span>a.</span>" +
          "<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
        "</span>" +
        "<span>Default numbered list item 3.</span>" +
      "</p>")).toBe(true);

    expect(outDocContents.includes(
      "<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" +
        "<span style=\"-aw-import:ignore\">" +
          "<span>2.1.1.1</span>" +
          "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
        "</span>" +
        "<span>Outline legal heading list item 5.</span>" +
      "</p>")).toBe(true);
    break;
  case aw.Saving.ExportListLabels.Auto:
    expect(outDocContents.includes(
      "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
        "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
          "<span>Default numbered list item 3.</span>" +
        "</li>" +
      "</ol>")).toBe(true);
    break;
  case aw.Saving.ExportListLabels.ByHtmlTags:
    expect(outDocContents.includes(
      "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
        "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
          "<span>Default numbered list item 3.</span>" +
        "</li>" +
      "</ol>")).toBe(true);
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../)
* property [HtmlSaveOptions.exportListLabels](../htmlsaveoptions/exportListLabels/)

