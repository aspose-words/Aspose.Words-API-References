---
title: Cell.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: .NET için Aspose.Words
description: İçerik yönetiminizi geliştirmek için, doğrudan alt paragraflardan ilk paragrafa zahmetsizce erişmek amacıyla Cell FirstParagraph özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.tables/cell/firstparagraph/
---
## Cell.FirstParagraph property

En yakın alt paragraflar arasında ilk paragrafı alır.

```csharp
public Paragraph FirstParagraph { get; }
```

## Örnekler

Belge oluşturucuyu kullanarak iç içe geçmiş tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dış tabloyu oluştur.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

// Dış tablonun ilk hücresine git, hücrenin içine başka bir tablo oluştur.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
