---
title: "FieldDatabase"
linktitle: "FieldDatabase"
second_title: "Aspose.Words для Java"
description: "Реализует поле DATABASE в Java."
type: docs
weight: 217
url: /ru/java/com.aspose.words/fielddatabase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldDatabase extends Field
```

Реализует поле DATABASE.

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Remarks:** 

Вставляет результаты запроса к базе данных в таблицу WordprocessingML.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getConnection()](#getConnection) | Получает соединение с данными. |
| [getDisplayResult()](#getDisplayResult) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFileName()](#getFileName) | Получает полный путь и имя файла базы данных |
| [getFirstRecord()](#getFirstRecord) | Получает целый номер первой записи данных для вставки. |
| [getFormat()](#getFormat) | Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [getFormatAttributes()](#getFormatAttributes) | Получает, какие атрибуты формата следует применить к таблице. |
| [getInsertHeadings()](#getInsertHeadings) | Получает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |
| [getInsertOnceOnMailMerge()](#getInsertOnceOnMailMerge) | Получает, следует ли вставлять данные в начало объединения. |
| [getLastRecord()](#getLastRecord) | Получает целый номер последней записи данных для вставки. |
| [getLocaleId()](#getLocaleId) | Получает LCID поля. |
| [getQuery()](#getQuery) | Получает набор инструкций SQL, которые запрашивают базу данных. |
| [getResult()](#getResult) | Получает текст, находящийся между разделителем поля и концом поля. |
| [getSeparator()](#getSeparator) | Получает узел, представляющий разделитель поля. |
| [getStart()](#getStart) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTableFormat()](#getTableFormat) | Получает формат, который будет применён к результату запроса к базе данных. |
| [getType()](#getType) | Получает тип поля Microsoft Word. |
| [isDirty()](#isDirty) | Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isDirty(boolean value)](#isDirty-boolean) | Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isLocked()](#isLocked) | Определяет, заблокировано ли поле (не должно пересчитывать свой результат). |
| [isLocked(boolean value)](#isLocked-boolean) | Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [remove()](#remove) | Удаляет поле из документа. |
| [setConnection(String value)](#setConnection-java.lang.String) | Устанавливает соединение с данными. |
| [setFileName(String value)](#setFileName-java.lang.String) | Устанавливает полный путь и имя файла базы данных |
| [setFirstRecord(String value)](#setFirstRecord-java.lang.String) | Устанавливает целочисленный номер первой записи данных для вставки. |
| [setFormatAttributes(String value)](#setFormatAttributes-java.lang.String) | Устанавливает, какие атрибуты формата следует применить к таблице. |
| [setInsertHeadings(boolean value)](#setInsertHeadings-boolean) | Устанавливает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |
| [setInsertOnceOnMailMerge(boolean value)](#setInsertOnceOnMailMerge-boolean) | Устанавливает, следует ли вставлять данные в начало слияния. |
| [setLastRecord(String value)](#setLastRecord-java.lang.String) | Устанавливает целочисленный номер последней записи данных для вставки. |
| [setLocaleId(int value)](#setLocaleId-int) | Устанавливает LCID поля. |
| [setQuery(String value)](#setQuery-java.lang.String) | Устанавливает набор SQL‑инструкций, которые запрашивают базу данных. |
| [setResult(String value)](#setResult-java.lang.String) | Устанавливает текст, находящийся между разделителем поля и его концом. |
| [setTableFormat(String value)](#setTableFormat-java.lang.String) | Устанавливает формат, который будет применён к результату запроса к базе данных. |
| [unlink()](#unlink) | Выполняет разъединение поля. |
| [update()](#update) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Выполняет обновление поля. |
### getConnection() {#getConnection}
```
public String getConnection()
```


Получает соединение с данными.

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

**Returns:**
java.lang.String — соединение с данными.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Получает текст, представляющий отображаемый результат поля.

 **Remarks:** 

Метод [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) должен быть вызван для получения корректного значения полей [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) и [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Показывает, как получить реальный текст, который поле отображает в документе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String — Текст, представляющий отображаемый результат поля.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Получает узел, представляющий конец поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат дочерних полей.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Показывает, как получить код поля.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует).

 **Examples:** 

Показывает, как получить код поля.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true, если коды дочерних полей должны быть включены. |

**Returns:**
java.lang.String
### getFileName() {#getFileName}
```
public String getFileName()
```


Получает полный путь и имя файла базы данных

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

**Returns:**
java.lang.String — полный путь и имя файла базы данных
### getFirstRecord() {#getFirstRecord}
```
public String getFirstRecord()
```


Получает целый номер первой записи данных для вставки.

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

**Returns:**
java.lang.String — целочисленный номер первой записи данных для вставки.
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля.

 **Examples:** 

Показывает, как форматировать результаты полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getFormatAttributes() {#getFormatAttributes}
```
public String getFormatAttributes()
```


Получает, какие атрибуты формата следует применить к таблице.

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

**Returns:**
java.lang.String — какие атрибуты формата следует применить к таблице.
### getInsertHeadings() {#getInsertHeadings}
```
public boolean getInsertHeadings()
```


Получает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице.

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

**Returns:**
boolean — следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице.
### getInsertOnceOnMailMerge() {#getInsertOnceOnMailMerge}
```
public boolean getInsertOnceOnMailMerge()
```


Получает, следует ли вставлять данные в начало объединения.

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

**Returns:**
boolean — следует ли вставлять данные в начало слияния.
### getLastRecord() {#getLastRecord}
```
public String getLastRecord()
```


Получает целый номер последней записи данных для вставки.

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

**Returns:**
java.lang.String — целочисленный номер последней записи данных для вставки.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Получает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - LCID поля.
### getQuery() {#getQuery}
```
public String getQuery()
```


Получает набор инструкций SQL, которые запрашивают базу данных.

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

**Returns:**
java.lang.String — набор SQL‑инструкций, которые запрашивают базу данных.
### getResult() {#getResult}
```
public String getResult()
```


Получает текст, находящийся между разделителем поля и концом поля.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Текст, который находится между разделителем поля и его концом.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель поля. Может быть  null .

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableFormat() {#getTableFormat}
```
public String getTableFormat()
```


Получает формат, который будет применён к результату запроса к базе данных.

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

**Returns:**
java.lang.String — формат, который будет применён к результату запроса к базе данных.
### getType() {#getType}
```
public int getType()
```


Получает тип поля Microsoft Word.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Тип поля Microsoft Word. Возвращаемое значение является одной из констант [FieldType](../../com.aspose.words/fieldtype/).
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Определяет, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Является ли поле заблокированным (не должно пересчитывать свой результат).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли поле заблокированным (не должно пересчитывать свой результат). |

### remove() {#remove}
```
public Node remove()
```


Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает  null .

 **Examples:** 

Показывает, как удалять поля из коллекции полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

Показывает, как обрабатывать поля PRIVATE.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setConnection(String value) {#setConnection-java.lang.String}
```
public void setConnection(String value)
```


Устанавливает соединение с данными.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соединение с данными. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


Устанавливает полный путь и имя файла базы данных

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Полный путь и имя файла базы данных |

### setFirstRecord(String value) {#setFirstRecord-java.lang.String}
```
public void setFirstRecord(String value)
```


Устанавливает целочисленный номер первой записи данных для вставки.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Целочисленный номер первой записи данных для вставки. |

### setFormatAttributes(String value) {#setFormatAttributes-java.lang.String}
```
public void setFormatAttributes(String value)
```


Устанавливает, какие атрибуты формата следует применить к таблице.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Какие атрибуты формата следует применить к таблице. |

### setInsertHeadings(boolean value) {#setInsertHeadings-boolean}
```
public void setInsertHeadings(boolean value)
```


Устанавливает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |

### setInsertOnceOnMailMerge(boolean value) {#setInsertOnceOnMailMerge-boolean}
```
public void setInsertOnceOnMailMerge(boolean value)
```


Устанавливает, следует ли вставлять данные в начало слияния.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Следует ли вставлять данные в начало слияния. |

### setLastRecord(String value) {#setLastRecord-java.lang.String}
```
public void setLastRecord(String value)
```


Устанавливает целочисленный номер последней записи данных для вставки.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Интегральный номер последней записи данных для вставки. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | LCID поля. |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Устанавливает набор SQL‑инструкций, которые запрашивают базу данных.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Набор SQL‑инструкций, которые запрашивают базу данных. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Устанавливает текст, находящийся между разделителем поля и его концом.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Текст, который находится между разделителем поля и его концом. |

### setTableFormat(String value) {#setTableFormat-java.lang.String}
```
public void setTableFormat(String value)
```


Устанавливает формат, который будет применён к результату запроса к базе данных.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Формат, который будет применён к результату запроса к базе данных. |

### unlink() {#unlink}
```
public boolean unlink()
```


Выполняет разъединение поля.

 **Remarks:** 

Заменяет поле его самым последним результатом.

Некоторые поля, такие как поля XE (Index Entry) и SEQ (Sequence), нельзя разъединять.

 **Examples:** 

Показывает, как разъединить поле.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  если поле было разъединено, иначе  false .
### update() {#update}
```
public void update()
```


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как вставить поле в документ, используя FieldType.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

Показывает, как форматировать результаты полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как сохранять или отбрасывать поля INCLUDEPICTURE при загрузке документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Если  true  то прямое форматирование результата поля отменяется, независимо от переключателя MERGEFORMAT, иначе выполняется обычное обновление. |

