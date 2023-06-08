---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words for .NET
description: MailMerge MergeDuplicateRegions property. Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one in C#.
type: docs
weight: 60
url: /net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to work with duplicate mail merge regions.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // If we set the "MergeDuplicateRegions" property to "false", the mail merge will affect the first region,
    // while the MERGEFIELDs of the second one will be left in the pre-merge state.
    // To get both regions merged like that,
    // we would have to execute the mail merge twice on a table of the same name.
    // If we set the "MergeDuplicateRegions" property to "true", the mail merge will affect both regions.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Returns a document that contains two duplicate mail merge regions (sharing the same name in the "TableStart/End" tags).
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
/// Creates a data table with one row and two columns.
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

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
