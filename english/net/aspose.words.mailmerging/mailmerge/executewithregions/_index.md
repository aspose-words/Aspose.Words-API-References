---
title: ExecuteWithRegions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 200
url: /net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge.ExecuteWithRegions method (1 of 6)

Performs a mail merge from a custom data source with mail merge regions.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | An object that implements the custom mail merge data source interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own class that implements the [`IMailMergeDataSource`](../../imailmergedatasource) interface.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate) is false, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

### See Also

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.ExecuteWithRegions method (2 of 6)

Performs a mail merge from a custom data source with mail merge regions.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | An object that implements the custom mail merge data source root interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own classes that implement the [`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot) and [`IMailMergeDataSource`](../../imailmergedatasource) interfaces.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate) is false, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

### See Also

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot)
* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.ExecuteWithRegions method (3 of 6)

Performs mail merge from a DataSet into a document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

### Remarks

Use this method to perform mail merge from one or more tables into repeatable mail merge regions in the document. The mail merge regions inside the document will dynamically grow to accommodate records in the corresponding tables.

Every table in the DataSet must have a name.

The document must have mail merge regions defined with names that refer to the tables in the DataSet.

To specify a mail merge region in the document you need to insert two mail merge fields to mark beginning and end of the mail merge region.

All document content that is included inside a mail merge region will be automatically repeated for every record in the DataTable.

To mark beginning of a mail merge region insert a MERGEFIELD with name TableStart:MyTable, where MyTable corresponds to one of the table names in your DataSet.

To mark the end of the mail merge region insert another MERGEFIELD with name TableEnd:MyTable.

To insert a MERGEFIELD in Word use Insert/Field command and select MergeField then type the name of the field.

The TableStart and TableEnd fields must be inside the same section in your document.

If used inside a table, TableStart and TableEnd must be inside the same row in the table.

Mail merge regions in a document should be well formed (there always needs to be a pair of matching TableStart and TableEnd merge fields with the same table name).

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.ExecuteWithRegions method (4 of 6)

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataTable | DataTable | Data source for the mail merge operation. The table must have its **TableName** property set. |

### Remarks

The document must have a mail merge region defined with name that matches **DataTable.TableName**.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.ExecuteWithRegions method (5 of 6)

Performs mail merge from a DataView into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataView | DataView | Data source for the mail merge operation. The source table of the **DataView** must have its **TableName** property set. |

### Remarks

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

The document must have a mail merge region defined with name that matches **DataView.Table.TableName**.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.ExecuteWithRegions method (6 of 6)

Performs mail merge from IDataReader into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | IDataReader | Source of the data records for mail merge such as OleDbDataReader or SqlDataReader. |
| tableName | String | Name of the mail merge region in the document to populate. |

### Remarks

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
