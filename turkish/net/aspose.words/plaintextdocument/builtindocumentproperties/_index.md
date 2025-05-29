---
title: PlainTextDocument.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: .NET için Aspose.Words
description: Gelişmiş belge organizasyonu için temel belge meta verilerine kolayca erişmek ve bunları yönetmek amacıyla PlainTextDocument BuiltInDocumentProperties özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Alır`BuiltInDocumentProperties` belgenin.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## Örnekler

Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini ve ardından orijinal belgenin yerleşik özelliklerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.BuiltInDocumentProperties.Author = "John Doe";

doc.Save(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("John Doe", plaintext.BuiltInDocumentProperties.Author);
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
