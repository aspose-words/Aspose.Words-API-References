---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: .NET için Aspose.Words
description: En son düzene göre toplam sayfa sayısını ortaya çıkaran ve doğru belge yönetimi ve içgörüler sağlayan Belge Sayfa Sayısı özelliğini keşfedin.
type: docs
weight: 330
url: /tr/net/aspose.words/document/pagecount/
---
## Document.PageCount property

En son sayfa düzeni işlemi tarafından hesaplanan belgedeki sayfa sayısını alır.

```csharp
public int PageCount { get; }
```

## Örnekler

Belgedeki sayfa sayısının nasıl sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Belgenin beklenen sayfa sayısını doğrulayın.
Assert.AreEqual(3, doc.PageCount);

// PageCount özelliğinin alınması, değeri hesaplamak için belgenin sayfa düzenini çağırdı.
// Belgeyi sabit bir sayfa kaydetme biçimine dönüştürürken bu işlemin tekrar yapılmasına gerek kalmayacaktır.
// .pdf gibi. Böylece özellikle daha karmaşık belgelerde biraz zaman kazanabilirsiniz.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Ayrıca bakınız

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
