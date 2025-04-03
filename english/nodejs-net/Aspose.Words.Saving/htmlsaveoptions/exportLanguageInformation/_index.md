---
title: HtmlSaveOptions.exportLanguageInformation property
linktitle: exportLanguageInformation property
articleTitle: exportLanguageInformation property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportLanguageInformation property. Specifies whether language information is exported to HTML, MHTML or EPUB"
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportLanguageInformation/
---

## HtmlSaveOptions.exportLanguageInformation property

Specifies whether language information is exported to HTML, MHTML or EPUB.
Default is ``false``.



```js
get exportLanguageInformation(): boolean
```

### Remarks

When this property is set to ``true`` Aspose.Words outputs **lang** HTML attribute on the document
elements that specify language. This can be needed to preserve language related semantics.




### Examples

Shows how to preserve language information when saving to .html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Use the builder to write text while formatting it in different locales.
builder.font.localeId = 1033; // en-US
builder.writeln("Hello world!");

builder.font.localeId = 2057; // en-GB
builder.writeln("Hello again!");

builder.font.localeId = 1049;// ru-RU
builder.write("Привет, мир!");

// When saving the document to HTML, we can pass a SaveOptions object
// to either preserve or discard each formatted text's locale.
// If we set the "ExportLanguageInformation" flag to "true",
// the output HTML document will contain the locales in "lang" attributes of <span> tags.
// If we set the "ExportLanguageInformation" flag to "false',
// the text in the output HTML document will not contain any locale information.
let options = new aw.Saving.HtmlSaveOptions();
options.exportLanguageInformation = exportLanguageInformation;
options.prettyFormat = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportLanguageInformation.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportLanguageInformation.html").toString();

if (exportLanguageInformation)
{
  expect(outDocContents.includes("<span>Hello world!</span>")).toEqual(true);
  expect(outDocContents.includes("<span lang=\"en-GB\">Hello again!</span>")).toEqual(true);
  expect(outDocContents.includes("<span lang=\"ru-RU\">Привет, мир!</span>")).toEqual(true);
}
else
{
  expect(outDocContents.includes("<span>Hello world!</span>")).toEqual(true);
  expect(outDocContents.includes("<span>Hello again!</span>")).toEqual(true);
  expect(outDocContents.includes("<span>Привет, мир!</span>")).toEqual(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

