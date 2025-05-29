---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: .NET için Aspose.Words
description: Hücre genişliğini değiştirmeden hücre stillerini varsayılana kolayca sıfırlamak için CellFormat ClearFormatting yöntemini keşfedin. E-tablo verimliliğinizi artırın!
type: docs
weight: 160
url: /tr/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Varsayılan hücre biçimlendirmesine sıfırlar. Hücrenin genişliğini değiştirmez.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
