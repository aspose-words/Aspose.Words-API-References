---
title: IFieldDatabaseProvider.GetQueryResult
second_title: Aspose.Words for .NET API Reference
description: IFieldDatabaseProvider method. Returns query result in C#.
type: docs
weight: 10
url: /net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Returns query result.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The complete path and file name of the database specified in the \d field switch. |
| connection | String | The connection to the data specified in the \c field switch. |
| query | String | The set of SQL instructions that query the database specified in the \s field switch. |
| field | FieldDatabase | The field being updated. |

### Return Value

The [`FieldDatabaseDataTable`](../../fielddatabasedatatable/) instance that should be used for the field's update.

### See Also

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* namespace [Aspose.Words.Fields](../../ifielddatabaseprovider/)
* assembly [Aspose.Words](../../../)
