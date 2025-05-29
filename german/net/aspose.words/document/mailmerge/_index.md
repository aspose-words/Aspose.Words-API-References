---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words für .NET
description: Schalten Sie mit dem MailMerge-Objekt eine nahtlose Dokumentenautomatisierung frei und verbessern Sie Ihren Arbeitsablauf, indem Sie Serienbriefaufgaben mühelos vereinfachen.
type: docs
weight: 270
url: /de/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Gibt einen[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) Objekt, das die Serienbrieffunktion für das Dokument darstellt.

```csharp
public MailMerge MailMerge { get; }
```

## Beispiele

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
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um für jede Zeile in der Tabelle ein Ausgabe-Seriendruckdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Serienbrief-Ausgabedokument zu erstellen:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
