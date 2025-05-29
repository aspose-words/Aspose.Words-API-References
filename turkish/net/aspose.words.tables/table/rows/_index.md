---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: .NET için Aspose.Words
description: Yazılı özelliğimizle tablo satırlarına zahmetsizce erişin, böylece projeleriniz için kusursuz veri yönetimi ve gelişmiş organizasyon sağlayın.
type: docs
weight: 260
url: /tr/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Tablonun satırlarına yazılmış erişim sağlar.

```csharp
public RowCollection Rows { get; }
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

Belgedeki tüm tablolarda nasıl gezinileceğini ve her hücrenin içeriğinin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Bir satır koleksiyonunu diziye kopyalamak için "ToArray" metodunu kullanabiliriz.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Bir hücre koleksiyonunu diziye kopyalamak için "ToArray" metodunu kullanabiliriz.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### Ayrıca bakınız

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
