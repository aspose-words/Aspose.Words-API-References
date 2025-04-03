---
title: HtmlSaveOptions.navigationMapLevel property
linktitle: navigationMapLevel property
articleTitle: navigationMapLevel property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.navigationMapLevel property. Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats"
type: docs
weight: 390
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/navigationMapLevel/
---

## HtmlSaveOptions.navigationMapLevel property

Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3
formats. Default value is ``3``.



```js
get navigationMapLevel(): number
```

### Remarks

The navigation map allows user agents to provide an easy way of navigation through the document structure.
Usually navigation points correspond to headings in the document. In order to populate headings up to level **N**
assign this value to [HtmlSaveOptions.navigationMapLevel](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2**
and **Heading 3**.
You can set this property to a value from 1 to 9 in order to request the corresponding maximum level.
Setting it to zero will reduce the navigation map to only the document root or roots of document parts.




### Examples

Shows how to generate table of contents for Azw3 documents.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Azw3);
options.navigationMapLevel = 2;

doc.save(base.artifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Shows how to generate table of contents for Mobi documents.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Mobi);
options.navigationMapLevel = 5;

doc.save(base.artifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Shows how to filter headings that appear in the navigation panel of a saved Epub document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Every paragraph that we format using a "Heading" style can serve as a heading.
// Each heading may also have a heading level, determined by the number of its heading style.
// The headings below are of levels 1-3.
builder.paragraphFormat.style = builder.document.styles.at("Heading 1");
builder.writeln("Heading #1");
builder.paragraphFormat.style = builder.document.styles.at("Heading 2");
builder.writeln("Heading #2");
builder.paragraphFormat.style = builder.document.styles.at("Heading 3");
builder.writeln("Heading #3");
builder.paragraphFormat.style = builder.document.styles.at("Heading 1");
builder.writeln("Heading #4");
builder.paragraphFormat.style = builder.document.styles.at("Heading 2");
builder.writeln("Heading #5");
builder.paragraphFormat.style = builder.document.styles.at("Heading 3");
builder.writeln("Heading #6");

// Epub readers typically create a table of contents for their documents.
// Each paragraph with a "Heading" style in the document will create an entry in this table of contents.
// We can use the "NavigationMapLevel" property to set a maximum heading level. 
// The Epub reader will not add headings with a level above the one we specify to the contents table.
let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Epub);
options.navigationMapLevel = 2;

// Our document has six headings, two of which are above level 2.
// The table of contents for this document will have four entries.
doc.save(base.artifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

