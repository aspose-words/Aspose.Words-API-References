---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words for .NET API Reference
description: MailMerge property. Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF fields condition in C#.
type: docs
weight: 140
url: /net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to merge fields or regions regardless of the parent IF field's condition.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a MERGEFIELD nested inside an IF field.
// Since the IF field statement is false, it will not display the result of the MERGEFIELD.
// The MERGEFIELD will also not receive any data during a mail merge.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// If we set the "UnconditionalMergeFieldsAndRegions" flag to "true",
// our mail merge will insert data into non-displayed fields such as our MERGEFIELD as well as all others.
// If we set the "UnconditionalMergeFieldsAndRegions" flag to "false",
// our mail merge will not insert data into MERGEFIELDs hidden by IF fields with false statements.
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

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
