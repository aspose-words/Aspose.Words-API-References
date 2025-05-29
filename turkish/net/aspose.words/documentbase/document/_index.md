---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Belgelerinizi verimli bir şekilde yönetmek için DocumentBase özelliklerini keşfedin. Sorunsuz erişimin kilidini açın ve iş akışınızı bugün geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Bu örneği alır.

```csharp
public override DocumentBase Document { get; }
```

## Örnekler

Basit bir belgenin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak en az düğüm kümesiyle birlikte gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: Bir Bölüm, Bir Gövde ve Bir Paragraf.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
