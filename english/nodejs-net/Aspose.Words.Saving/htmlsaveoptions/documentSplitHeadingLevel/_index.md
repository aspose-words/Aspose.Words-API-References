---
title: HtmlSaveOptions.documentSplitHeadingLevel property
linktitle: documentSplitHeadingLevel property
articleTitle: documentSplitHeadingLevel property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.documentSplitHeadingLevel property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/documentSplitHeadingLevel/
---

## HtmlSaveOptions.documentSplitHeadingLevel property

Specifies the maximum level of headings at which to split the document.
Default value is ``2``.



```js
get documentSplitHeadingLevel(): number
```

### Remarks

When [HtmlSaveOptions.documentSplitCriteria](../documentSplitCriteria/) includes [DocumentSplitCriteria.HeadingParagraph](../../documentsplitcriteria/#HeadingParagraph) 
and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using 
**Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. 
Setting this property to zero will cause the document not to be split at heading paragraphs at all.




### Examples

Shows how to split an output HTML document by headings into several parts.

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

// Create a HtmlSaveOptions object and set the split criteria to "HeadingParagraph".
// These criteria will split the document at paragraphs with "Heading" styles into several smaller documents,
// and save each document in a separate HTML file in the local file system.
// We will also set the maximum heading level, which splits the document to 2.
// Saving the document will split it at headings of levels 1 and 2, but not at 3 to 9.
let options = new aw.Saving.HtmlSaveOptions();
options.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.HeadingParagraph;
options.documentSplitHeadingLevel = 2;

// Our document has four headings of levels 1 - 2. One of those headings will not be
// a split point since it is at the beginning of the document.
// The saving operation will split our document at three places, into four smaller documents.
doc.save(base.artifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new aw.Document(base.artifactsDir + "HtmlSaveOptions.HeadingLevels.html");

expect(doc.getText().trim()).toEqual("Heading #1");

doc = new aw.Document(base.artifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

expect(doc.getText().trim()).toEqual("Heading #2\r" +
                        "Heading #3");

doc = new aw.Document(base.artifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

expect(doc.getText().trim()).toEqual("Heading #4");

doc = new aw.Document(base.artifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

expect(doc.getText().trim()).toEqual("Heading #5\r" +
                        "Heading #6");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.documentSplitCriteria](../documentSplitCriteria/)
* property [HtmlSaveOptions.documentPartSavingCallback](../documentPartSavingCallback/)

