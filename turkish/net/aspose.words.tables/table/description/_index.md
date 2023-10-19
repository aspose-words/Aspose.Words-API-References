---
title: Table.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words for .NET
description: Table Description mülk. Bu tablonun açıklamasını alır veya ayarlar. Tabloda yer alan bilgilerin alternatif metin gösterimini sağlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.tables/table/description/
---
## Table.Description property

Bu tablonun açıklamasını alır veya ayarlar. Tabloda yer alan bilgilerin alternatif metin gösterimini sağlar.

```csharp
public string Description { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Bu özellik ISO/IEC 29500 uyumlu DOCX belgeleri ( için anlamlıdır.[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). ISO/IEC 29500 öncesi formatlara kaydedildiğinde özellik göz ardı edilir.

## Örnekler

Belge oluşturucu kullanmadan iç içe tablonun nasıl oluşturulacağını gösterir.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Üç satır ve dört sütundan oluşan dış tabloyu oluşturup belgeye ekleyin.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // İki satır ve iki sütundan oluşan başka bir tablo oluşturun ve bunu ilk tablonun ilk hücresine ekleyin.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Her hücrede verilen boyut ve metinle belgede yeni bir tablo oluşturur.
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

    // Tablonuza sırasıyla başlık ve açıklama eklemek için "Başlık" ve "Açıklama" özelliklerini kullanabilirsiniz.
    // Bu özellikleri kullanabilmemiz için tablonun en az bir satıra sahip olması gerekir.
    // Bu özellikler ISO/IEC 29500 uyumlu .docx belgeleri için anlamlıdır (bkz. OoxmlCompliance sınıfı).
    // Belgeyi ISO/IEC 29500 öncesi formatlarda kaydedersek, Microsoft Word bu özellikleri göz ardı eder.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
