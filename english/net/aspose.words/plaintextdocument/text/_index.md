---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Access the PlainTextDocument's text property to retrieve the document's content as a single string, enhancing your data handling and analysis.
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

Assert.That(plaintext.Text.Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
