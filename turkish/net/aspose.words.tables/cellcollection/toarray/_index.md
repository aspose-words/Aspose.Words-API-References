---
title: CellCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: .NET için Aspose.Words
description: ToArray metoduyla CellCollection'ınızı zahmetsizce yeni bir diziye dönüştürerek veri yönetimini kolaylaştırın ve performansı artırın.
type: docs
weight: 20
url: /tr/net/aspose.words.tables/cellcollection/toarray/
---
## CellCollection.ToArray method

Koleksiyondaki tüm hücreleri yeni bir hücre dizisine kopyalar.

```csharp
public Cell[] ToArray()
```

### Geri dönüş değeri

Bir hücre dizisi.

## Örnekler

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

* class [Cell](../../cell/)
* class [CellCollection](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
