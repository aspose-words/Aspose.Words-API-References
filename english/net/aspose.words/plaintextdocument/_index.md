---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.PlainTextDocument class. Allows to extract plaintext representation of the documents content in C#.
type: docs
weight: 4350
url: /net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Allows to extract plain-text representation of the document's content.

To learn more, visit the [Working with Text Document](https://docs.aspose.com/words/net/working-with-text-document/) documentation article.

```csharp
public class PlainTextDocument
```

## Constructors

| Name | Description |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Creates a plain text document from a stream. Automatically detects the file format. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Creates a plain text document from a file. Automatically detects the file format. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Creates a plain text document from a stream. Allows to specify additional options such as an encryption password. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Creates a plain text document from a file. Allows to specify additional options such as an encryption password. |

## Properties

| Name | Description |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Gets [`BuiltInDocumentProperties`](./builtindocumentproperties/) of the document. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Gets [`CustomDocumentProperties`](./customdocumentproperties/) of the document. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Gets textual content of the document concatenated as a string. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
