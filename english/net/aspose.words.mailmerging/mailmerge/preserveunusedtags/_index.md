---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words for .NET
description: Discover the MailMerge PreserveUnusedTags property to manage unused mustache tags effectively, enhancing your document automation process.
type: docs
weight: 80
url: /net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Gets or sets a value indicating whether the unused "mustache" tags should be preserved.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Remarks

The default value is `false`.

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
}

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

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
