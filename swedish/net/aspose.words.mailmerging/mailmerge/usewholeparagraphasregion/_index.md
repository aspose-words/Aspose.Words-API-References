---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen UseWholeParagraphAsRegion i MailMerge för att förbättra dina områden för koppling av dokument och säkerställa fullständig kontroll över innehållets inkludering.
type: docs
weight: 160
url: /sv/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Hämtar eller anger ett värde som anger om hela stycket med**Tabellstart** eller**Bordände** field eller ett visst intervall mellan**Tabellstart** och**Bordände** fält ska inkluderas i området för koppling av dokument.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

## Exempel

Visar förhållandet mellan områden för dokumentkoppling och stycken.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Som standard kan ett stycke tillhöra högst ett dokumentkopplingsområde.
    // Innehållet i vårt dokument uppfyller inte dessa kriterier.
    // Om vi ställer in flaggan "UseWholeParagraphAsRegion" till "sant",
    // att köra en dokumentkoppling på det här dokumentet kommer att utlösa ett undantag.
    // Om vi ställer in flaggan "UseWholeParagraphAsRegion" till "false",
    // vi kommer att kunna utföra en dokumentkoppling på det här dokumentet.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Kopplad utskrifter fyller vår första region medan den andra regionen lämnas oanvänd
    // eftersom det är regionen som bryter mot regeln.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Skapa ett dokument med två områden för dokumentkoppling som delar ett stycke.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Skapa en datatabell som kan fylla i en region under en dokumentkoppling.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
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
