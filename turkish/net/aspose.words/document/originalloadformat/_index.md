---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: .NET için Aspose.Words
description: Nesnenize yüklenen orijinal belgenin biçimine kolayca erişmek ve belge yönetimini geliştirmek için OriginalLoadFormat özelliğini keşfedin.
type: docs
weight: 310
url: /tr/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Bu nesneye yüklenen orijinal belgenin biçimini alır.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Notlar

Yeni boş bir belge oluşturduysanız, şunu döndürür:Doc değer.

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
