---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: .NET için Aspose.Words
description: Gelişmiş elektronik tablo tasarımı ve işlevselliği için hücre kenarlığı koleksiyonlarına erişmek ve bunları özelleştirmek üzere CellFormat Borders özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Hücrenin kenarlıklarının koleksiyonunu alır.

```csharp
public BorderCollection Borders { get; }
```

## Örnekler

İki tablodaki satırların nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Aşağıda bir belgeden tablo almanın iki yolu bulunmaktadır.
// 1 - Bir Body düğümünün "Tablolar" koleksiyonundan:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - "GetChild" metodunu kullanarak:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Mevcut tablodaki tüm satırları bir sonrakine ekle.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Boş tablo kabını kaldır.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Ayrıca bakınız

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
