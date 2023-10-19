---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words for .NET
description: Document MailMerge mülk. Bir değeri döndürürMailMerge belgenin adresmektup birleştirme işlevini temsil eden nesne C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Bir değeri döndürür[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) belgenin adres-mektup birleştirme işlevini temsil eden nesne.

```csharp
public MailMerge MailMerge { get; }
```

## Örnekler

DataTable'daki verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres-mektup birleştirme için veri kaynağı olarak DataTable'ı kullanmanın iki yolu verilmiştir.
    // 1 - Tablodaki her satır için bir çıktı adres-mektup birleştirme belgesi oluşturmak amacıyla adres-mektup birleştirme için tablonun tamamını kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres-mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres-mektup birleştirme kaynak belgesi oluşturur.
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
