---
title: "FieldDatabaseDataTable"
linktitle: "FieldDatabaseDataTable"
second_title: "Aspose.Words لـ Java"
description: "يوفر بيانات لنتيجة الحقل FieldDatabase في Java."
type: docs
weight: 219
url: /ar/java/com.aspose.words/fielddatabasedatatable/
---

**Inheritance:**
java.lang.Object
```
public class FieldDatabaseDataTable
```

يوفر البيانات لنتيجة الحقل [FieldDatabase](../../com.aspose.words/fielddatabase/). يرجى الاطلاع على مثيل [DataTable](../../com.aspose.words.net.system.data/datatable/).

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fields ][Working with Fields].

 **Examples:** 

يعرض كيفية استخراج البيانات من قاعدة بيانات وإدراجها كحقل في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This DATABASE field will run a query on a database, and display the result in a table.
 FieldDatabase field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getDatabaseDir() + "Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT * FROM [Products]");

 Assert.assertEquals(MessageFormat.format(" DATABASE  \\d {0} \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", getDatabaseDir().replace("\\", "\\\\") + "Northwind.accdb"),
         field.getFieldCode());

 // Insert another DATABASE field with a more complex query that sorts all products in descending order by gross sales.
 field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getMyDir() + "Database\\Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
         "FROM([Products] " +
         "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
         "GROUP BY[Products].ProductName " +
         "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC");

 // These properties have the same function as LIMIT and TOP clauses.
 // Configure them to display only rows 1 to 10 of the query result in the field's table.
 field.setFirstRecord("1");
 field.setLastRecord("10");

 // This property is the index of the format we want to use for our table. The list of table formats is in the "Table AutoFormat..." menu
 // that shows up when we create a DATABASE field in Microsoft Word. Index #10 corresponds to the "Colorful 3" format.
 field.setTableFormat("10");

 // The FormatAttribute property is a string representation of an integer which stores multiple flags.
 // We can patrially apply the format which the TableFormat property points to by setting different flags in this property.
 // The number we use is the sum of a combination of values corresponding to different aspects of the table style.
 // 63 represents 1 (borders) + 2 (shading) + 4 (font) + 8 (color) + 16 (autofit) + 32 (heading rows).
 field.setFormatAttributes("63");
 field.setInsertHeadings(true);
 field.setInsertOnceOnMailMerge(true);

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.DATABASE.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [FieldDatabaseDataTable(String[] columnNames)](#FieldDatabaseDataTable-java.lang.String...) | ينشئ مثيلًا جديدًا للفئة [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [createFrom(System.Data.DataTable dataTable)](#createFrom-com.aspose.words.net.System.Data.DataTable) | ينشئ مثيلًا جديدًا للفئة [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) من مثيل [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnNames()](#getColumnNames) | يحصل على الأعمدة التي تنتمي إلى هذا الجدول. |
| [getRows()](#getRows) | يحصل على الصفوف التي تنتمي إلى هذا الجدول. |
### FieldDatabaseDataTable(String[] columnNames) {#FieldDatabaseDataTable-java.lang.String...}
```
public FieldDatabaseDataTable(String[] columnNames)
```


ينشئ مثيلًا جديدًا للفئة [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnNames | java.lang.String[] |  |

### createFrom(System.Data.DataTable dataTable) {#createFrom-com.aspose.words.net.System.Data.DataTable}
```
public static FieldDatabaseDataTable createFrom(System.Data.DataTable dataTable)
```


ينشئ مثيلًا جديدًا للفئة [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) من مثيل [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/)
### getColumnNames() {#getColumnNames}
```
public String[] getColumnNames()
```


يحصل على الأعمدة التي تنتمي إلى هذا الجدول.

**Returns:**
java.lang.String[] - الأعمدة التي تنتمي إلى هذا الجدول.
### getRows() {#getRows}
```
public ArrayList getRows()
```


يحصل على الصفوف التي تنتمي إلى هذا الجدول.

**Returns:**
java.util.ArrayList - الصفوف التي تنتمي إلى هذا الجدول.
