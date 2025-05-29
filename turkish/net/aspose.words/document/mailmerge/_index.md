---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: .NET için Aspose.Words
description: MailMerge nesnesiyle kusursuz belge otomasyonunun kilidini açın ve posta birleştirme görevlerini zahmetsizce basitleştirerek iş akışınızı geliştirin.
type: docs
weight: 270
url: /tr/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Bir[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) belge için posta birleştirme işlevini temsil eden nesne.

```csharp
public MailMerge MailMerge { get; }
```

## Örnekler

DataTable'daki verilerle posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda bir posta birleştirme için veri kaynağı olarak DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablonun tamamını kullanarak, tablodaki her satır için tek bir çıktı birleştirme belgesi oluşturun:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Tablonun bir satırını kullanarak tek bir çıktı birleştirme belgesi oluşturun:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Bir posta birleştirme kaynak belgesi oluşturur.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ayrıca bakınız

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
