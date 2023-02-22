---
title: Table.Table
second_title: Aspose.Words for .NET API Referansı
description: Table inşaatçı. Yeni bir örneğini başlatır Masa sınıf.
type: docs
weight: 10
url: /tr/net/aspose.words.tables/table/table/
---
## Table constructor

Yeni bir örneğini başlatır **Masa** sınıf.

```csharp
public Table(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

### Notlar

Ne zaman **Masa** oluşturulur, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değil ve **Üst Düğüm** boş.

Eklemek **Masa** belgeye, tablonun eklenmesini istediğiniz hikayede InsertAfter veya InsertBefore kullanın.

### Örnekler

Bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, paragraflar içerebilen hücreler içeren satırlar içerir
// koşular, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Bir tabloda "EnsureMinimum" yöntemini çağırmak,
// tabloda en az bir satır, hücre ve paragraf var.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Tablonun ilk satırındaki ilk aramaya metin ekleyin.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Belge oluşturucu kullanmadan iç içe tablonun nasıl oluşturulacağını gösterir.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Üç satır ve dört sütunlu dış tabloyu oluşturun ve ardından belgeye ekleyin.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // İki satır ve iki sütun içeren başka bir tablo oluşturun ve ardından bunu ilk tablonun ilk hücresine ekleyin.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Her hücrede verilen boyutlar ve metin ile belgede yeni bir tablo oluşturur.
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

    // Tablonuza sırasıyla başlık ve açıklama eklemek için "Title" ve "Description" özelliklerini kullanabilirsiniz.
    // Bu özellikleri kullanabilmemiz için tablonun en az bir satırı olmalıdır.
    // Bu özellikler, ISO/IEC 29500 uyumlu .docx belgeleri için anlamlıdır (bkz. OoxmlCompliance sınıfı).
    // Belgeyi ISO/IEC 29500 öncesi formatlarda kaydedersek, Microsoft Word bu özellikleri yok sayar.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


