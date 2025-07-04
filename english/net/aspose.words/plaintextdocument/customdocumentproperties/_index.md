---
title: PlainTextDocument.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words for .NET
description: Discover how to access CustomDocumentProperties in PlainTextDocument for enhanced document management and customization. Unlock your document's potential!
type: docs
weight: 30
url: /net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

Gets `CustomDocumentProperties` of the document.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## Examples

Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's custom properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.CustomDocumentProperties.Add("Location of writing", "123 Main St, London, UK");

doc.Save(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

Assert.That(plaintext.Text.Trim(), Is.EqualTo("Hello world!"));
Assert.That(plaintext.CustomDocumentProperties["Location of writing"].Value, Is.EqualTo("123 Main St, London, UK"));
```

### See Also

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
