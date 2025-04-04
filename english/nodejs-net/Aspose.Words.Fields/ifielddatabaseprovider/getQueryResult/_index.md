---
title: IFieldDatabaseProvider.getQueryResult method
linktitle: getQueryResult method
articleTitle: getQueryResult method
second_title: Aspose.Words for Node.js
description: "IFieldDatabaseProvider.getQueryResult method. Returns query result."
type: docs
weight: 10
url: /nodejs-net/aspose.words.fields/ifielddatabaseprovider/getQueryResult/
---

## getQueryResult(fileName, connection, query, field) {#string_string_string_fielddatabase}

Returns query result.


```js
getQueryResult(fileName: string, connection: string, query: string, field: Aspose.Words.Fields.FieldDatabase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The complete path and file name of the database specified in the \\d field switch. |
| connection | string | The connection to the data specified in the \\c field switch. |
| query | string | The set of SQL instructions that query the database specified in the \\s field switch. |
| field | [FieldDatabase](../../fielddatabase/) | The field being updated. |

### Returns

The [FieldDatabaseDataTable](../../fielddatabasedatatable/) instance that should be used for the field's update.


### See Also

* module [Aspose.Words.Fields](../../)
* class [IFieldDatabaseProvider](../)

