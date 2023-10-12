---
title: Document.MailMerge
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Returnerar enMailMerge objekt som representerar kopplingsfunktionen för dokumentet.
type: docs
weight: 260
url: /sv/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Returnerar en[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) objekt som representerar kopplingsfunktionen för dokumentet.

```csharp
public MailMerge MailMerge { get; }
```

### Exempel

Visar hur man kör en e-postsammanfogning med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan finns två sätt att använda en datatabell som datakälla för en e-postkoppling.
    // 1 - Använd hela tabellen för kopplingen för att skapa ett kopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett dokument för utmatning av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för sammankoppling av brev.
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
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


