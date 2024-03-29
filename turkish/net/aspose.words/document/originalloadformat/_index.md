---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words for .NET
description: Document OriginalLoadFormat mülk. Bu nesneye yüklenen orijinal belgenin biçimini alır C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Bu nesneye yüklenen orijinal belgenin biçimini alır.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Notlar

Yeni bir boş belge oluşturduysanız,Doc değer.

## Örnekler

Bir belgenin yükleme işleminin ayrıntılarının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Ayrıca bakınız

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
