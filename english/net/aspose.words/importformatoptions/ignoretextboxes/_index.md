---
title: ImportFormatOptions.IgnoreTextBoxes
second_title: Aspose.Words for .NET API Reference
description: ImportFormatOptions property. Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if KeepSourceFormatting mode is used. The default value is true in C#.
type: docs
weight: 40
url: /net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if KeepSourceFormatting mode is used. The default value is `true`.

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Examples

Shows how to manage text box formatting while appending a document.

```csharp
// Create a document that will have nodes from another document inserted into it.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Create another document with a text box, which we will import into the first document.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Set a flag to specify whether to clear or preserve text box formatting
// while importing them to other documents.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Import the text box from the source document into the destination document,
// and then verify whether we have preserved the styling of its text contents.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../importformatoptions/)
* assembly [Aspose.Words](../../../)
