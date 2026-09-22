---
title: "DataTableEventListener"
linktitle: "DataTableEventListener"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا للعمل مع EventListeners عندما يتم تغيير DataTable في Java."
type: docs
weight: 33
url: /ar/java/com.aspose.words.net.system.data/datatableeventlistener/
---
```
public interface DataTableEventListener
```

يوفر طرقًا للعمل مع EventListeners عندما يتم تغيير [DataTable](../../com.aspose.words.net.system.data/datatable/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) | تحديث المستمع عند حذف DataColumn |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) | تحديث المستمع عند إدراج DataColumn |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) | تحديث المستمع عند تعديل DataRow |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) | تحديث المستمع عند حذف DataRow |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) | تحديث المستمع عند إدراج DataRow |
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public abstract void onDataColumnDeleted(System.Data.DataColumn column)
```


تحديث المستمع عند حذف DataColumn

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public abstract void onDataColumnInserted(System.Data.DataColumn column)
```


تحديث المستمع عند إدراج DataColumn

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public abstract void onDataRowChanged(System.Data.DataRow row)
```


تحديث المستمع عند تعديل DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public abstract void onDataRowDeleted(System.Data.DataRow row)
```


تحديث المستمع عند حذف DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public abstract void onDataRowInserted(System.Data.DataRow row)
```


تحديث المستمع عند إدراج DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

