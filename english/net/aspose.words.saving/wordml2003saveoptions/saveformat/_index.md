---
title: WordML2003SaveOptions.SaveFormat
linktitle: SaveFormat
second_title: Aspose.Words for .NET API Reference
description: WordML2003SaveOptions SaveFormat property. Specifies the format in which the document will be saved if this save options object is used. Can only be WordML in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/wordml2003saveoptions/saveformat/
---
## SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can only be WordML.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Examples

Shows how to manage output document's raw content.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Set the "PrettyFormat" property to "true" to apply tab character indentation and
// newlines to make the output document's raw content easier to read.
// Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");

if (prettyFormat)
    Assert.True(fileContents.Contains(
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
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [WordML2003SaveOptions](../)
* namespace [Aspose.Words.Saving](../../wordml2003saveoptions/)
* assembly [Aspose.Words](../../../)
