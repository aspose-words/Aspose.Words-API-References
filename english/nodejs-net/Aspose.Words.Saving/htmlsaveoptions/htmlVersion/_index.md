---
title: HtmlSaveOptions.htmlVersion property
linktitle: htmlVersion property
articleTitle: htmlVersion property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.htmlVersion property. Specifies version of HTML standard that should be used when saving the document to HTML or MHTML"
type: docs
weight: 330
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/htmlVersion/
---

## HtmlSaveOptions.htmlVersion property

Specifies version of HTML standard that should be used when saving the document to HTML or MHTML.
Default value is [HtmlVersion.Xhtml](../../htmlversion/#Xhtml).



```js
get htmlVersion(): Aspose.Words.Saving.HtmlVersion
```

### Examples

Shows how to save a document to a specific version of HTML.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.htmlVersion = htmlVersion,
options.prettyFormat = true

doc.save(base.artifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// Our HTML documents will have minor differences to be compatible with different HTML versions.
let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.HtmlVersions.html").toString();

switch (htmlVersion)
{
  case aw.Saving.HtmlVersion.Html5:
    expect(outDocContents.includes("<a id=\"_Toc76372689\"></a>")).toEqual(true);
    expect(outDocContents.includes("<a id=\"_Toc76372689\"></a>")).toEqual(true);
    expect(outDocContents.includes("<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">")).toEqual(true);
    break;
  case aw.Saving.HtmlVersion.Xhtml:
    expect(outDocContents.includes("<a name=\"_Toc76372689\"></a>")).toEqual(true);
    expect(outDocContents.includes("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">")).toEqual(true);
    expect(outDocContents.includes("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\"")).toEqual(true);
    break;
}
```

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.htmlVersion = aw.Saving.HtmlVersion.Xhtml;
options.exportXhtmlTransitional = showDoctypeDeclaration;
options.prettyFormat = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportXhtmlTransitional.html", options);

// Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportXhtmlTransitional.html").toString();

if (showDoctypeDeclaration)
  expect(outDocContents.includes(
    "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
    "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
    "<html xmlns=\"http://www.w3.org/1999/xhtml\">")).toEqual(true);
else
  expect(outDocContents.includes("<html>")).toEqual(true);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

