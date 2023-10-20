---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words för .NET
description: MailMerge MergeWholeDocument fast egendom. Hämtar eller ställer in ett värde som indikerar om fält i hela dokumentet uppdateras under körning av en sammankoppling med regioner i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Hämtar eller ställer in ett värde som indikerar om fält i hela dokumentet uppdateras under körning av en sammankoppling med regioner.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar förhållandet mellan e-postsammanslagningar med regioner och fältuppdatering.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Om vi sätter "MergeWholeDocument"-flaggan till "true",
    // sammanslagningen med regioner kommer att uppdatera alla fält i dokumentet.
    // Om vi ställer in "MergeWholeDocument"-flaggan till "false", kommer e-postkopplingen endast att uppdatera fält
    // inom kopplingsområdet vars namn matchar namnet på datakälltabellen.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Brevkopplingen kommer endast att uppdatera fältet CITAT utanför kopplingsområdet
    // om vi sätter "MergeWholeDocument"-flaggan till "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Skapa ett dokument med en kopplingsregion som tillhör en datakälla som heter "MyTable".
/// Infoga ett CITAT-fält i denna region och ytterligare ett utanför det.
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
/// Skapa en datatabell som kommer att användas i en sammanslagning.
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
