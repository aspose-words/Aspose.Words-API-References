---
title: HtmlSaveOptions.exportRoundtripInformation property
linktitle: exportRoundtripInformation property
articleTitle: exportRoundtripInformation property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportRoundtripInformation property. Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB"
type: docs
weight: 240
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportRoundtripInformation/
---

## HtmlSaveOptions.exportRoundtripInformation property

Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB.
Default value is ``True`` for HTML and ``False`` for MHTML and EPUB.



```js
get exportRoundtripInformation(): boolean
```

### Remarks

Saving of the roundtrip information allows to restore document properties such as tab stops,
comments, headers and footers during the HTML documents loading back into a [Document](../../../Aspose.Words/document/) object.

When ``True``, the roundtrip information is exported as -aw-\* CSS properties
of the corresponding HTML elements.

When ``False``, causes no roundtrip information to be output into produced files.




### Examples

Shows how to preserve hidden elements when converting to .html.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
// or footnotes will be either removed or converted to plain text and effectively be lost.
// Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.

// When we save the document to HTML, we can pass a SaveOptions object to determine
// how the saving operation will export document elements that HTML does not support or use,
// such as hidden bookmarks and original shape positions.
// If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
// If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
// We will want to preserve such elements if we intend to load the saved HTML using Aspose.words,
// as they could be of use once again.
let options = new aw.Saving.HtmlSaveOptions();
options.exportRoundtripInformation = exportRoundtripInformation;

doc.save(base.artifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.RoundTripInformation.html").toString();
doc = new aw.Document(base.artifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
  expect(outDocContents.includes("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">")).toEqual(true);
  expect(outDocContents.includes("<span style=\"-aw-import:ignore\">&#xa0;</span>")).toEqual(true);

  expect(outDocContents.includes(
                "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
                "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
                "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">")).toEqual(true);

  expect(outDocContents.includes(
                "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">")).toEqual(true);

  expect(outDocContents.includes(
                "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />")).toEqual(true);


  expect(outDocContents.includes(
                "<span>Page number </span>" +
                "<span style=\"-aw-field-start:true\"></span>" +
                "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
                "<span style=\"-aw-field-separator:true\"></span>" +
                "<span>1</span>" +
                "<span style=\"-aw-field-end:true\"></span>")).toEqual(true);

  expect([...doc.range.fields].filter(f => f.type == aw.Fields.FieldType.FieldPage).length).toEqual(1);
}
else
{
  expect(outDocContents.includes("<div style=\"clear:both\">")).toEqual(true);
  expect(outDocContents.includes("<span>&#xa0;</span>")).toEqual(true);

  expect(outDocContents.includes(
                "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
                "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">")).toEqual(true);

  expect(outDocContents.includes(
                "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">")).toEqual(true);

  expect(outDocContents.includes(
                "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />")).toEqual(true);

  expect(outDocContents.includes(
                "<span>Page number 1</span>")).toEqual(true);

  expect([...doc.range.fields].filter(f => f.type == aw.Fields.FieldType.FieldPage).length).toEqual(0);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

