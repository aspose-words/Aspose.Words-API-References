---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words för .NET
description: Upptäck hur MailMerges egenskap UnconditionalMergeFieldsAndRegions förbättrar dokumentautomation genom att sammanfoga fält och regioner utan villkorliga begränsningar.
type: docs
weight: 140
url: /sv/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Hämtar eller anger ett värde som anger om sammanslagningsfält och sammanslagningsområden slås samman oavsett det överordnade OM-fältets villkor.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man sammanfogar fält eller regioner oavsett det överordnade OM-fältets villkor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEFIELD kapslat inuti ett OM-fält.
// Eftersom IF-fältsatsen är falsk kommer den inte att visa resultatet av MERGEFIELD.
// MERGEFIELD kommer inte heller att ta emot några data under en dokumentkoppling.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Om vi ställer in flaggan "UnconditionalMergeFieldsAndRegions" till "sant",
// vår dokumentkoppling infogar data i fält som inte visas, såsom vårt MERGEFIELD samt alla andra.
// Om vi ställer in flaggan "UnconditionalMergeFieldsAndRegions" till "false",
// vår dokumentkoppling kommer inte att infoga data i MERGEFIELDS som är dolda av OM-fält med falska påståenden.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
