---
title: "MailMerge"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 3560
url: /net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Represents the mail merge functionality.

```csharp
public class MailMerge
```

## Public Members

| Name | Description |
| --- | --- |
| [CleanupOptions](cleanupoptions) { get; set; } | Gets or sets a set of flags that specify what items should be removed during mail merge. |
| [CleanupParagraphsWithPunctuationMarks](cleanupparagraphswithpunctuationmarks) { get; set; } | Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the RemoveEmptyParagraphs option is specified. |
| [FieldMergingCallback](fieldmergingcallback) { get; set; } | Occurs during mail merge when a mail merge field is encountered in the document. |
| [MailMergeCallback](mailmergecallback) { get; set; } | Allows to handle particular events during mail merge. |
| [MappedDataFields](mappeddatafields) { get; } | Returns a collection that represents mapped data fields for the mail merge operation. |
| [MergeDuplicateRegions](mergeduplicateregions) { get; set; } | Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [MergeWholeDocument](mergewholedocument) { get; set; } | Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [PreserveUnusedTags](preserveunusedtags) { get; set; } | Gets or sets a value indicating whether the unused "mustache" tags should be preserved. |
| [RegionEndTag](regionendtag) { get; set; } | Gets or sets a mail merge region end tag. |
| [RegionStartTag](regionstarttag) { get; set; } | Gets or sets a mail merge region start tag. |
| [RestartListsAtEachSection](restartlistsateachsection) { get; set; } | Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [RetainFirstSectionStart](retainfirstsectionstart) { get; set; } | Gets or sets a value indicating whether the [`SectionStart`](../../aspose.words/pagesetup/sectionstart) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [TrimWhitespaces](trimwhitespaces) { get; set; } | Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [UnconditionalMergeFieldsAndRegions](unconditionalmergefieldsandregions) { get; set; } | Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [UseNonMergeFields](usenonmergefields) { get; set; } | When true, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags. |
| [UseWholeParagraphAsRegion](usewholeparagraphasregion) { get; set; } | Gets or sets a value indicating whether whole paragraph with TableStart or TableEnd field or particular range between TableStart and TableEnd fields should be included into mail merge region. |
| [DeleteFields](deletefields)() | Removes mail merge related fields from the document. |
| [Execute](execute)(…) | Performs a mail merge from a custom data source. (6 methods) |
| [ExecuteWithRegions](executewithregions)(…) | Performs a mail merge from a custom data source with mail merge regions. (6 methods) |
| [GetFieldNames](getfieldnames)() | Returns a collection of mail merge field names available in the document. |
| [GetFieldNamesForRegion](getfieldnamesforregion)(…) | Returns a collection of mail merge field names available in the region. (2 methods) |
| [GetRegionsByName](getregionsbyname)(…) | Returns a collection of mail merge regions with the specified name. |
| [GetRegionsHierarchy](getregionshierarchy)() | Returns a full hierarchy of regions (with fields) available in the document. |

### Remarks

For mail merge operation to work, the document should contain Word MERGEFIELD and optionally NEXT fields. During mail merge operation, merge fields in the document are replaced with values from your data source.There are two distinct ways to use mail merge: with mail merge regions and without.The simplest mail merge is without regions and it is very similar to how mail merge works in Word. Use Execute methods to merge information from some data source such as DataTable, DataSet, DataView, IDataReader or an array of objects into your document. The MailMerge object processes all records of the data source and copies and appends content of the whole document for each record.Note that when MailMerge object encounters a NEXT field, it selects next record in the data source and continues merging without copying any content.Use ExecuteWithRegions methods to merge information into a document with mail merge regions defined. You can use DataSet, DataTable, DataView or IDataReader as data sources for this operation.You need to use mail merge regions if you want to dynamically grow portions inside the document. Without mail merge regions whole document will be repeated for every record of the data source.

### Examples

Shows how to execute a mail merge with data from a DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Below are two ways of using a DataTable as the data source for a mail merge.
    // 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 -  Use one row of the table to create one output mail merge document:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Creates a mail merge source document.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
