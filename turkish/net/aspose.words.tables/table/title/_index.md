---
title: Table.Title
linktitle: Title
articleTitle: Title
second_title: .NET için Aspose.Words
description: Tablo Başlığı özelliğini keşfedin, gelişmiş erişilebilirlik ve gelişmiş veri gösterimi için tablonuzun başlığını kolayca ayarlayın veya değiştirin.
type: docs
weight: 320
url: /tr/net/aspose.words.tables/table/title/
---
## Table.Title property

Bu tablonun başlığını alır veya ayarlar. Tabloda bulunan bilgilerin alternatif bir metin gösterimini sağlar.

```csharp
public string Title { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Bu özellik, ISO/IEC 29500 uyumlu DOCX belgeleri ( için anlamlıdır[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). ISO/IEC 29500 öncesi biçimlerde kaydedildiğinde, özellik yok sayılır.

## Örnekler

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

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
