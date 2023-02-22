---
title: MailMerge.UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words för .NET API Referens
description: MailMerge fast egendom. Hämtar eller ställer in ett värde som anger om sammanslagningsfält och sammanslagningsregioner slås samman oavsett det överordnade IFfältets tillstånd.
type: docs
weight: 140
url: /sv/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Hämtar eller ställer in ett värde som anger om sammanslagningsfält och sammanslagningsregioner slås samman oavsett det överordnade IF-fältets tillstånd.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

### Anmärkningar

Standardvärdet är **falsk** .

### Exempel

Visar hur man slår samman fält eller regioner oavsett det överordnade IF-fältets tillstånd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEFIELD kapslat i ett IF-fält.
// Eftersom IF-fältsatsen är falsk kommer den inte att visa resultatet av MERGEFIELD.
// MERGEFIELD kommer inte heller att ta emot några data under en e-postsammanfogning.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Om vi ställer in flaggan "UnconditionalMergeFieldsAndRegions" till "true",
// vår sammanslagning kommer att infoga data i icke-visade fält som vårt MERGEFIELD såväl som alla andra.
// Om vi ställer in flaggan "UnconditionalMergeFieldsAndRegions" till "false",
// vår sammanslagning kommer inte att infoga data i MERGEFIELDs dolda av IF-fält med falska uttalanden.
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
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


