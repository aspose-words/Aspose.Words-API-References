---
title: Table.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: .NET için Aspose.Words
description: Tablonuz ile çevresindeki metin arasındaki boşlukları noktalar halinde kontrol etmek, düzeni ve okunabilirliği artırmak için Table DistanceRight özelliğini ayarlayın.
type: docs
weight: 140
url: /tr/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

Tablonun sağ tarafı ile çevresindeki metin arasındaki mesafeyi puan cinsinden alır veya ayarlar.

```csharp
public double DistanceRight { get; set; }
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
