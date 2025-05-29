---
title: Table
linktitle: Table
articleTitle: Table
second_title: .NET için Aspose.Words
description: Sezgisel Tablo Oluşturucumuzla zahmetsizce özel tablolar oluşturun. Verilerinizin görüntülenmesini dakikalar içinde oluşturun, özelleştirin ve optimize edin!
type: docs
weight: 10
url: /tr/net/aspose.words.tables/table/table/
---
## Table constructor

Yeni bir örneğini başlatır[`Table`](../) sınıf.

```csharp
public Table(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Ne zaman[`Table`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../../aspose.words/node/parentnode/) dır`hükümsüz`.

Eklemek için[`Table`](../) belge kullanımına[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) veya[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)Tablonun eklenmesini istediğiniz hikayede .

## Örnekler

Bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, hücreler içeren satırlar ve bu satırların içinde paragraflar olabilir
// tipik elemanlar olan koşular, şekiller ve hatta diğer tablolar ile.
// Bir tabloda "EnsureMinimum" metodunu çağırmak,
// tabloda en az bir satır, hücre ve paragraf var.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Tablonun ilk satırındaki ilk hücreye metin ekle.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Belge oluşturucu kullanmadan iç içe geçmiş tablonun nasıl oluşturulacağını gösterir.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Üç satır ve dört sütundan oluşan dış tabloyu oluştur ve ardından bunu belgeye ekle.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // İki satır ve iki sütundan oluşan başka bir tablo oluştur ve bunu ilk tablonun ilk hücresine ekle.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Belgede, her hücrede belirtilen boyutlar ve metinle yeni bir tablo oluşturur.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Tablonuza sırasıyla bir başlık ve açıklama eklemek için "Başlık" ve "Açıklama" özelliklerini kullanabilirsiniz.
    // Bu özellikleri kullanabilmemiz için tablonun en az bir satırının olması gerekir.
    // Bu özellikler ISO/IEC 29500 uyumlu .docx belgeleri için anlamlıdır (OoxmlCompliance sınıfına bakın).
    // Belgeyi ISO/IEC 29500 öncesi biçimlerde kaydedersek, Microsoft Word bu özellikleri yoksayar.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
