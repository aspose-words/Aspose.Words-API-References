---
title: Document.MailMerge
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Gibt a zurückMailMerge Objekt das die Serienbrieffunktion für das Dokument darstellt.
type: docs
weight: 260
url: /de/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Gibt a zurück[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) Objekt, das die Serienbrieffunktion für das Dokument darstellt.

```csharp
public MailMerge MailMerge { get; }
```

### Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nachfolgend finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Serienbrief zu verwenden.
    // 1 – Verwenden Sie die gesamte Tabelle für den Serienbrief, um für jede Zeile in der Tabelle ein Ausgabe-Serienbriefdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 – Verwenden Sie eine Zeile der Tabelle, um ein Ausgabe-Serienbriefdokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Serienbrief-Quelldokument.
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

### Siehe auch

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


