---
title: MappedDataFieldCollection
second_title: Aspose.Words for .NET API Reference
description: Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.
type: docs
weight: 3600
url: /net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item) { get; set; } | Gets or sets the name of the field in the data source associated with the specified mail merge field. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add)(string, string) | Adds a new field mapping. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear)() | Removes all elements from the collection. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey)(string) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue)(string) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator)() | Returns a dictionary enumerator object that can be used to iterate over all items in the collection. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove)(string) | Removes a field mapping. |

## Remarks

This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.

## Examples

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // The table has a column named "Column2", but there are no MERGEFIELDs with that name.
    // Also, we have a MERGEFIELD named "Column3", but the data source does not have a column with that name.
    // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
    // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // We can link a data source column name to a MERGEFIELD name like this.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Link the data source column named "Column2" to MERGEFIELDs named "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // The MERGEFIELD name is the "key" to the respective data source column name "value".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // We can iterate over the elements in this collection.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // We can also remove elements from the collection.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Create a document with 2 MERGEFIELDs, one of which does not have a
/// corresponding column in the data table from the method below.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Create a data table with 2 columns, one of which does not have a
/// corresponding MERGEFIELD in the source document from the method above.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
