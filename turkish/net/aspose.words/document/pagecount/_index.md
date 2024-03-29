---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words for .NET
description: Document PageCount mülk. En son sayfa düzeni işlemiyle hesaplanan belgedeki sayfa sayısını alır C#'da.
type: docs
weight: 320
url: /tr/net/aspose.words/document/pagecount/
---
## Document.PageCount property

En son sayfa düzeni işlemiyle hesaplanan belgedeki sayfa sayısını alır.

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
// Belgeyi sabit sayfa kaydetme formatına dönüştürürken bu işlemin yeniden yapılmasına gerek kalmayacak,
// .pdf gibi. Böylece, özellikle daha karmaşık belgelerde biraz zaman kazanabilirsiniz.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Ayrıca bakınız

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
