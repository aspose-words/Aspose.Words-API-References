---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: Veri işleme ve analizinizi geliştirmek için, PlainTextDocument'in text özelliğine erişerek belgenin içeriğini tek bir dize olarak alın.
type: docs
weight: 40
url: /tr/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Belgenin metinsel içeriğini bir dize olarak birleştirilmiş olarak alır.

```csharp
public string Text { get; }
```

## Örnekler

Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

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
