---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words för .NET
description: Optimera din dokumentkopplingsprocess med egenskapen MergeDuplicateRegions. Styr hur datakällregioner slås samman för effektiv dokumenthantering.
type: docs
weight: 60
url: /sv/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Hämtar eller anger ett värde som anger om alla dokumentkopplingsområden med namnet på en datakälla ska slås samman vid utskriftskoppling med regioner mot datakällan eller bara den första.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man arbetar med dubbletter av dokumentkopplingsområden.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Om vi ställer in egenskapen "MergeDuplicateRegions" till "false" kommer dokumentkopplingen att påverka den första regionen,
    // medan MERGEFIELDS för den andra kommer att lämnas i tillståndet före sammanslagningen.
    // För att få båda regionerna sammanslagna på det sättet,
    // vi skulle behöva köra dokumentkopplingen två gånger på en tabell med samma namn.
    // Om vi ställer in egenskapen "MergeDuplicateRegions" till "true" kommer dokumentkopplingen att påverka båda regionerna.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Returnerar ett dokument som innehåller två dubbletter av dokumentkopplingsområden (som delar samma namn i taggarna "TableStart/End").
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Skapar en datatabell med en rad och två kolumner.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
