---
title: WordML2003SaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for NodeJs
description: "WordML2003SaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/wordml2003saveoptions/saveFormat/
---

## WordML2003SaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.WordML](../../../aspose.words/saveformat/#WordML).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to manage output document's raw content.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
let options = new aw.Saving.WordML2003SaveOptions();

expect(options.saveFormat).toEqual(aw.SaveFormat.WordML);

// Set the "PrettyFormat" property to "true" to apply tab character indentation and
// newlines to make the output document's raw content easier to read.
// Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options.prettyFormat = prettyFormat;

doc.save(base.artifactsDir + "WordML2003SaveOptions.prettyFormat.xml", options);

let fileContents = fs.readFileSync(base.artifactsDir + "WordML2003SaveOptions.prettyFormat.xml").toString();

if (prettyFormat)
  expect(fileContents).toEqual(expect.stringContaining(
    "<o:DocumentProperties>\r\n\t\t" +
      "<o:Revision>1</o:Revision>\r\n\t\t" +
      "<o:TotalTime>0</o:TotalTime>\r\n\t\t" +
      "<o:Pages>1</o:Pages>\r\n\t\t" +
      "<o:Words>0</o:Words>\r\n\t\t" +
      "<o:Characters>0</o:Characters>\r\n\t\t" +
      "<o:Lines>1</o:Lines>\r\n\t\t" +
      "<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" +
      "<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" +
      "<o:Version>11.5606</o:Version>\r\n\t" +
    "</o:DocumentProperties>"));
else
  expect(fileContents).toEqual(expect.stringContaining(
     "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
     "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
     "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [WordML2003SaveOptions](../)

