---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen MailMerge MergeWholeDocument uppdaterar alla fält under en regionsbaserad dokumentkoppling, vilket förbättrar effektiviteten och noggrannheten i dina dokument.
type: docs
weight: 70
url: /sv/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Hämtar eller anger ett värde som anger om fält i hela dokumentet uppdateras när en dokumentkoppling med regioner utförs.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar sambandet mellan dokumentkopplingar med regioner och fältuppdatering.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Om vi ställer in flaggan "MergeWholeDocument" till "sant",
    // dokumentkopplingen med regioner kommer att uppdatera alla fält i dokumentet.
    // Om vi ställer in flaggan "MergeWholeDocument" till "false" kommer dokumentkopplingen bara att uppdatera fält
    // inom den kopplingsregion vars namn matchar namnet på datakällstabellen.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Koppla dokument uppdaterar endast fältet CITAT utanför kopplingsområdet
    // om vi sätter flaggan "MergeWholeDocument" till "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Skapa ett dokument med en region för dokumentkoppling som tillhör en datakälla med namnet "Min tabell".
/// Infoga ett QUOTE-fält inuti den här regionen och ett till utanför den.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Skapa en datatabell som ska användas i en dokumentkoppling.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
