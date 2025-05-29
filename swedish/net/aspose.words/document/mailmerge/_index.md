---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words för .NET
description: Lås upp sömlös dokumentautomation med MailMerge-objektet, vilket förbättrar ditt arbetsflöde genom att förenkla dokumentkopplingsuppgifter utan ansträngning.
type: docs
weight: 270
url: /sv/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Returnerar en[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) objekt som representerar dokumentkopplingsfunktionen för dokumentet.

```csharp
public MailMerge MailMerge { get; }
```

## Exempel

Visar hur man utför en dokumentkoppling med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan följer två sätt att använda en datatabell som datakälla för en dokumentkoppling.
    // 1 - Använd hela tabellen för dokumentkopplingen för att skapa ett utgående dokumentkopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett enda dokument för koppling av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för dokumentkoppling.
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

### Se även

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
