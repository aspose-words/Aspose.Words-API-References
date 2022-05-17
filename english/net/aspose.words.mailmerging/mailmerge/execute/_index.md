---
title: Execute
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 180
url: /net/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge.Execute method (1 of 6)

Performs a mail merge from a custom data source.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | An object that implements the custom mail merge data source interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from any data source such as a list or hashtable or objects. You need to write your own class that implements the [`IMailMergeDataSource`](../../imailmergedatasource) interface.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate) is false, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the RemoveUnusedRegions option.

### See Also

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (2 of 6)

Performs a mail merge operation for a single record.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldNames | String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| values | Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

Use this method to fill mail merge fields in the document with values from an array of objects.

This method merges data for one record only. The array of field names and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the RemoveUnusedRegions option.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (3 of 6)

Performs mail merge from a DataTable into the document.

```csharp
public void Execute(DataTable table)
```

| Parameter | Type | Description |
| --- | --- | --- |
| table | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### Remarks

Use this method to fill mail merge fields in the document with values from a **DataTable**.

All records from the table are merged into the document.

You can use NEXT field in the Word document to cause **MailMerge** object to select next record from the **DataTable** and continue merging. This can be used when creating documents such as mailing labels.

When **MailMerge** object reaches end of the main document and there are still more rows in the **DataTable**, it copies entire content of the main document and appends it to the end of the destination document using a section break as a separator.

This method ignores the RemoveUnusedRegions option.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (4 of 6)

Performs mail merge from IDataReader into the document.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | IDataReader | Data source for the mail merge operation. |

### Remarks

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the RemoveUnusedRegions option.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (5 of 6)

Performs mail merge from a DataView into the document.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataView | DataView | Data source for the mail merge operation. |

### Remarks

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the RemoveUnusedRegions option.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (6 of 6)

Performs mail merge from a DataRow into the document.

```csharp
public void Execute(DataRow row)
```

| Parameter | Type | Description |
| --- | --- | --- |
| row | DataRow | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### Remarks

Use this method to fill mail merge fields in the document with values from a **DataRow**.

This method ignores the RemoveUnusedRegions option.

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
