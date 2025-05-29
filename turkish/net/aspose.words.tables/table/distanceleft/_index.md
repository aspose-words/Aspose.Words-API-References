---
title: Table.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: .NET için Aspose.Words
description: Tablonuz ile çevresindeki metin arasındaki boşluğu kontrol etmek için Table DistanceLeft özelliğini ayarlayın. Belgelerinizdeki okunabilirliği ve düzeni geliştirin!
type: docs
weight: 130
url: /tr/net/aspose.words.tables/table/distanceleft/
---
## Table.DistanceLeft property

Tablonun solu ile çevresindeki metin arasındaki mesafeyi noktalar halinde alır veya ayarlar.

```csharp
public double DistanceLeft { get; set; }
```

## Örnekler

Tablo sınırları ile metin arasındaki mesafenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// Tablo ile çevresindeki metin arasındaki mesafeyi ayarlayın.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
