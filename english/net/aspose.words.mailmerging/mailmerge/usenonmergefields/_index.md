---
title: MailMerge.UseNonMergeFields
second_title: Aspose.Words for .NET API Reference
description: MailMerge property. When true specifies that in addition to MERGEFIELD fields mail merge is performed into some other types of fields and also into fieldName tags in C#.
type: docs
weight: 150
url: /net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

When `true`, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Remarks

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When `UseNonMergeFields` is set to `true`, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when `UseNonMergeFields` is set to `true`, Aspose.Words will perform mail merge into text tags "{{fieldName}}". These are not fields, but just text tags.

## Examples

Shows how to preserve the appearance of alternative mail merge tags that go unused during a mail merge.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

    // By default, a mail merge places data from each row of a table into MERGEFIELDs, which name columns in that table. 
    // Our document has no such fields, but it does have plaintext tags enclosed by curly braces.
    // If we set the "PreserveUnusedTags" flag to "true", we could treat these tags as MERGEFIELDs
    // to allow our mail merge to insert data from the data source at those tags.
    // If we set the "PreserveUnusedTags" flag to "false",
    // the mail merge will convert these tags to MERGEFIELDs and leave them unfilled.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Our document has a tag for a column named "Column2", which does not exist in the table.
    // If we set the "PreserveUnusedTags" flag to "false", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));

/// <summary>
/// Create a document and add two plaintext tags that may act as MERGEFIELDs during a mail merge.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Our tags will register as destinations for mail merge data only if we set this to true.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Create a simple data table with one column.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
