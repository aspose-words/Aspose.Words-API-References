---
title: "FieldDatabaseDataTable"
linktitle: "FieldDatabaseDataTable"
second_title: "Aspose.Words для Java"
description: "Предоставляет данные для результата поля FieldDatabase в Java."
type: docs
weight: 219
url: /ru/java/com.aspose.words/fielddatabasedatatable/
---

**Inheritance:**
java.lang.Object
```
public class FieldDatabaseDataTable
```

Предоставляет данные для результата поля [FieldDatabase](../../com.aspose.words/fielddatabase/). Пожалуйста, смотрите экземпляр [DataTable](../../com.aspose.words.net.system.data/datatable/).

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Examples:** 

Показывает, как извлечь данные из базы данных и вставить их в виде поля в документ.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FieldDatabaseDataTable(String[] columnNames)](#FieldDatabaseDataTable-java.lang.String...) | Инициализирует новый экземпляр класса [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/). |
## Методы

| Метод | Описание |
| --- | --- |
| [createFrom(System.Data.DataTable dataTable)](#createFrom-com.aspose.words.net.System.Data.DataTable) | Инициализирует новый экземпляр класса [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) из экземпляра [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnNames()](#getColumnNames) | Получает столбцы, принадлежащие этой таблице. |
| [getRows()](#getRows) | Получает строки, принадлежащие этой таблице. |
### FieldDatabaseDataTable(String[] columnNames) {#FieldDatabaseDataTable-java.lang.String...}
```
public FieldDatabaseDataTable(String[] columnNames)
```


Инициализирует новый экземпляр класса [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnNames | java.lang.String[] |  |

### createFrom(System.Data.DataTable dataTable) {#createFrom-com.aspose.words.net.System.Data.DataTable}
```
public static FieldDatabaseDataTable createFrom(System.Data.DataTable dataTable)
```


Инициализирует новый экземпляр класса [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) из экземпляра [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/)
### getColumnNames() {#getColumnNames}
```
public String[] getColumnNames()
```


Получает столбцы, принадлежащие этой таблице.

**Returns:**
java.lang.String[] — Столбцы, принадлежащие этой таблице.
### getRows() {#getRows}
```
public ArrayList getRows()
```


Получает строки, принадлежащие этой таблице.

**Returns:**
java.util.ArrayList — Строки, принадлежащие этой таблице.
