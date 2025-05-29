---
title: Row
linktitle: Row
articleTitle: Row
second_title: .NET için Aspose.Words
description: Row oluşturucumuzla dinamik Row örneklerini kolayca oluşturun. Veri yönetiminizi basitleştirin ve kodlama verimliliğinizi bugün artırın!
type: docs
weight: 10
url: /tr/net/aspose.words.tables/row/row/
---
## Row constructor

Yeni bir örneğini başlatır[`Row`](../) sınıf.

```csharp
public Row(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Ne zaman[`Row`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../../aspose.words/node/parentnode/) dır`hükümsüz`.

Eklemek için[`Row`](../) belge kullanımına[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) veya[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)Satırın eklenmesini istediğiniz tabloda .

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
