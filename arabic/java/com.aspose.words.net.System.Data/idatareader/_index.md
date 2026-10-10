---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words لـ Java"
description: "يوفر وسيلة لقراءة تدفق واحد أو أكثر من تدفقات النتائج ذات الاتجاه الواحد التي يتم الحصول عليها بتنفيذ أمر على مصدر البيانات ويتم تنفيذها بواسطة موفري بيانات .NET Framework الذين يصلون إلى قواعد البيانات العلائقية في Java."
type: docs
weight: 34
url: /ar/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

يوفر وسيلة لقراءة تدفق واحد أو أكثر من تدفقات النتائج ذات الاتجاه الواحد التي يتم الحصول عليها بتنفيذ أمر على مصدر البيانات، ويتم تنفيذها بواسطة موفري بيانات .NET Framework الذين يصلون إلى قواعد البيانات العلائقية.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [close()](#close) | يغلق كائن [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [getDepth()](#getDepth) | يحصل على قيمة تشير إلى عمق التداخل للصف الحالي. |
| [getRecordsAffected()](#getRecordsAffected) | يحصل على عدد الصفوف التي تم تعديلها أو إدراجها أو حذفها نتيجة تنفيذ جملة SQL. |
| [getSchemaTable()](#getSchemaTable) | يرجع [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يصف بيانات تعريف الأعمدة لـ [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | يحصل على قيمة تشير إلى ما إذا كان قارئ البيانات مغلقًا. |
| [nextResult()](#nextResult) | ينقل قارئ البيانات إلى النتيجة التالية عند قراءة نتائج عبارات SQL المجمعة. |
| [read()](#read) | ينقل [IDataReader](../../com.aspose.words.net.system.data/idatareader/) إلى السجل التالي. |
### close() {#close}
```
public abstract void close()
```


يغلق كائن [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


يحصل على قيمة تشير إلى عمق التداخل للصف الحالي.

**Returns:**
int - مستوى التداخل.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


يحصل على عدد الصفوف التي تم تعديلها أو إدراجها أو حذفها نتيجة تنفيذ جملة SQL.

**Returns:**
int - عدد الصفوف التي تم تعديلها أو إدراجها أو حذفها؛ 0 إذا لم تتأثر أي صفوف أو فشلت العبارة؛ و -1 لعبارات SELECT.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


يرجع [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يصف بيانات تعريف الأعمدة لـ [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


يحصل على قيمة تشير إلى ما إذا كان قارئ البيانات مغلقًا.

**Returns:**
boolean - true إذا كان قارئ البيانات مغلقًا؛ وإلا false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


ينقل قارئ البيانات إلى النتيجة التالية عند قراءة نتائج عبارات SQL المجمعة.

**Returns:**
boolean - true إذا كان هناك المزيد من الصفوف؛ وإلا false.
### read() {#read}
```
public abstract boolean read()
```


ينقل [IDataReader](../../com.aspose.words.net.system.data/idatareader/) إلى السجل التالي.

**Returns:**
boolean - true إذا كان هناك المزيد من الصفوف؛ وإلا false.
