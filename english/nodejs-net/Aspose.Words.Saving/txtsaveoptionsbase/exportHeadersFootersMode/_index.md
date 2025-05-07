---
title: TxtSaveOptionsBase.exportHeadersFootersMode property
linktitle: exportHeadersFootersMode property
articleTitle: exportHeadersFootersMode property
second_title: Aspose.Words for Node.js
description: "TxtSaveOptionsBase.exportHeadersFootersMode property. Specifies the way headers and footers are exported to the text formats"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/txtsaveoptionsbase/exportHeadersFootersMode/
---

## TxtSaveOptionsBase.exportHeadersFootersMode property

Specifies the way headers and footers are exported to the text formats.
Default value is [TxtExportHeadersFootersMode.PrimaryOnly](../../txtexportheadersfootersmode/#PrimaryOnly).



```js
get exportHeadersFootersMode(): Aspose.Words.Saving.TxtExportHeadersFootersMode
```

### Examples

Shows how to specify how to export headers and footers to plain text format.

```js
let doc = new aw.Document();

// Insert even and primary headers/footers into the document.
// The primary header/footers will override the even headers/footers.
doc.firstSection.headersFooters.add(new aw.HeaderFooter(doc, aw.HeaderFooterType.HeaderEven));
doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderEven).appendParagraph("Even header");
doc.firstSection.headersFooters.add(new aw.HeaderFooter(doc, aw.HeaderFooterType.FooterEven));
doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterEven).appendParagraph("Even footer");
doc.firstSection.headersFooters.add(new aw.HeaderFooter(doc, aw.HeaderFooterType.HeaderPrimary));
doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderPrimary).appendParagraph("Primary header");
doc.firstSection.headersFooters.add(new aw.HeaderFooter(doc, aw.HeaderFooterType.FooterPrimary));
doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary).appendParagraph("Primary footer");

// Insert pages to display these headers and footers.
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Page 1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2");
builder.insertBreak(aw.BreakType.PageBreak); 
builder.write("Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let saveOptions = new aw.Saving.TxtSaveOptions();

// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
// to not export any headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
// to only export primary headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
// to place all headers and footers for all section bodies at the end of the document.
saveOptions.exportHeadersFootersMode = txtExportHeadersFootersMode;

doc.save(base.artifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
  case aw.Saving.TxtExportHeadersFootersMode.AllAtEnd:
    expect(docText).toEqual("Page 1\r\n" +
                                "Page 2\r\n" +
                                "Page 3\r\n" +
                                "Even header\r\n\r\n" +
                                "Primary header\r\n\r\n" +
                                "Even footer\r\n\r\n" +
                                "Primary footer\r\n\r\n");
    break;
  case aw.Saving.TxtExportHeadersFootersMode.PrimaryOnly:
    expect(docText).toEqual("Primary header\r\n" +
                                "Page 1\r\n" +
                                "Page 2\r\n" +
                                "Page 3\r\n" +
                                "Primary footer\r\n");
    break;
  case aw.Saving.TxtExportHeadersFootersMode.None:
    expect(docText).toEqual("Page 1\r\n" +
                                "Page 2\r\n" +
                                "Page 3\r\n");
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptionsBase](../)

