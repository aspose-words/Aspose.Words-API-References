---
title: PlainTextDocument.Text
linktitle: Text
second_title: Aspose.Words for .NET API Reference
description: PlainTextDocument Text property. Gets textual content of the document concatenated as a string in C#.
type: docs
weight: 40
url: /net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Gets textual content of the document concatenated as a string.

```csharp
public string Text { get; }
```

## Examples

Shows how to load the contents of a Microsoft Word document in plaintext.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### See Also

* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../plaintextdocument/)
* assembly [Aspose.Words](../../../)
