---
title: MappedDataFieldCollection.Add
linktitle: Add
second_title: Aspose.Words for .NET API Reference
description: MappedDataFieldCollection method. Adds a new field mapping in C#.
type: docs
weight: 30
url: /net/aspose.words.mailmerging/mappeddatafieldcollection/add/
---
## MappedDataFieldCollection.Add method

Adds a new field mapping.

```csharp
public void Add(string documentFieldName, string dataSourceFieldName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | String | Case-sensitive name of the mail merge field in the document. |
| dataSourceFieldName | String | Case-sensitive name of the field in the data source. |

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

* class [MappedDataFieldCollection](../)
* namespace [Aspose.Words.MailMerging](../../mappeddatafieldcollection/)
* assembly [Aspose.Words](../../../)
