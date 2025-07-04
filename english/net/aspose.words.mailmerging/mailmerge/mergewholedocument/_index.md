---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words for .NET
description: Discover how the MailMerge MergeWholeDocument property updates all fields during a region-based mail merge, enhancing efficiency and accuracy in your documents.
type: docs
weight: 70
url: /net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows the relationship between mail merges with regions, and field updating.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // If we set the "MergeWholeDocument" flag to "true",
    // the mail merge with regions will update every field in the document.
    // If we set the "MergeWholeDocument" flag to "false", the mail merge will only update fields
    // within the mail merge region whose name matches the name of the data source table.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // The mail merge will only update the QUOTE field outside of the mail merge region
    // if we set the "MergeWholeDocument" flag to "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.That(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."), Is.True);
    Assert.That(doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."), Is.EqualTo(mergeWholeDocument));
}

/// <summary>
/// Create a document with a mail merge region that belongs to a data source named "MyTable".
/// Insert one QUOTE field inside this region, and one more outside it.
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
/// Create a data table that will be used in a mail merge.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
