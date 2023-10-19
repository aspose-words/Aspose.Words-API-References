---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: CellFormat ClearFormatting yöntem. Varsayılan hücre formatına sıfırlar. Hücrenin genişliğini değiştirmez C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Varsayılan hücre formatına sıfırlar. Hücrenin genişliğini değiştirmez.

```csharp
public void ClearFormatting()
```

## Örnekler

İki tablodaki satırların nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Aşağıda bir belgeden tablo almanın iki yolu verilmiştir.
// 1 - Bir Gövde düğümünün "Tablolar" koleksiyonundan:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - "GetChild" yöntemini kullanarak:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Geçerli tablodaki tüm satırları sonrakine ekle.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Boş masa kabını çıkarın.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Ayrıca bakınız

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
