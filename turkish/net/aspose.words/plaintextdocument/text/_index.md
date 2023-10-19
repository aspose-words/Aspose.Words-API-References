---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: PlainTextDocument Text mülk. Belgenin metin içeriğini bir dize olarak birleştirir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Belgenin metin içeriğini bir dize olarak birleştirir.

```csharp
public string Text { get; }
```

## Örnekler

Bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ayrıca bakınız

* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
