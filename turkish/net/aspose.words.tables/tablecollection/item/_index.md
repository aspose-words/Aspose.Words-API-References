---
title: TableCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Belirli dizinlerdeki tabloları alarak TableCollection öğelerine zahmetsizce erişin. Sezgisel özellik özelliğimizle veri yönetiminizi basitleştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.tables/tablecollection/item/
---
## TableCollection indexer

Birini alır[`Table`](../../table/) verilen indekste.

```csharp
public Table this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

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

* class [Table](../../table/)
* class [TableCollection](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
