---
title: "MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words для Java"
description: "Позволяет автоматически сопоставлять имена полей в вашем источнике данных с именами полей слияния в документе в Java."
type: docs
weight: 448
url: /ru/java/com.aspose.words/mappeddatafieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Позволяет автоматически сопоставлять имена полей в вашем источнике данных с именами полей слияния почты в документе.

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Это реализовано как коллекция строковых ключей и строковых значений. Ключи — это имена полей слияния в документе, а значения — имена полей в вашем источнике данных.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Методы

| Метод | Описание |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String) | Добавляет новое сопоставление полей. |
| [clear()](#clear) | Удаляет все элементы из коллекции. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String) | Определяет, существует ли сопоставление указанного поля в документе в коллекции. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String) | Определяет, существует ли сопоставление указанного поля в источнике данных в коллекции. |
| [get(String documentFieldName)](#get-java.lang.String) | Получает имя поля в источнике данных, связанного с указанным полем слияния. |
| [getCount()](#getCount) | Получает количество элементов, содержащихся в коллекции. |
| [iterator()](#iterator) | Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции. |
| [remove(String documentFieldName)](#remove-java.lang.String) | Удаляет сопоставление полей. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String) | Устанавливает имя поля в источнике данных, связанного с указанным полем слияния. |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Добавляет новое сопоставление полей.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния почты в документе. |
| dataSourceFieldName | java.lang.String | Регистрозависимое имя поля в источнике данных. |

### clear() {#clear}
```
public void clear()
```


Удаляет все элементы из коллекции.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

### containsKey(String documentFieldName) {#containsKey-java.lang.String}
```
public boolean containsKey(String documentFieldName)
```


Определяет, существует ли сопоставление указанного поля в документе в коллекции.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния почты в документе. |

**Returns:**
boolean -  true  если элемент найден в коллекции; иначе,  false .
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String}
```
public boolean containsValue(String dataSourceFieldName)
```


Определяет, существует ли сопоставление указанного поля в источнике данных в коллекции.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Регистрозависимое имя поля в источнике данных. |

**Returns:**
boolean -  true  если элемент найден в коллекции; иначе,  false .
### get(String documentFieldName) {#get-java.lang.String}
```
public String get(String documentFieldName)
```


Получает имя поля в источнике данных, связанного с указанным полем слияния.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Returns:**
java.lang.String — имя поля в источнике данных, связанное с указанным полем слияния почты.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Returns:**
int — количество элементов, содержащихся в коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Returns:**
java.util.Iterator
### remove(String documentFieldName) {#remove-java.lang.String}
```
public void remove(String documentFieldName)
```


Удаляет сопоставление полей.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния почты в документе. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String documentFieldName, String value)
```


Устанавливает имя поля в источнике данных, связанного с указанным полем слияния.

 **Examples:** 

Показывает, как сопоставлять столбцы данных и MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния.

```

 public void mappedDataFieldCollection() throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMappedDataFields();
     DataTable dataTable = createSourceTableMappedDataFields();

     // We have a column "Column2" in the data table that doesn't have a respective MERGEFIELD in the document
     // Also, we have a MERGEFIELD named "Column3" that does not exist as a column in the data source
     // If data from "Column2" is suitable for the "Column3" MERGEFIELD,
     // we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair
     MappedDataFieldCollection mappedDataFields = doc.getMailMerge().getMappedDataFields();

     // A data source column name is linked to a MERGEFIELD name by adding an element like this
     mappedDataFields.add("MergeFieldName", "DataSourceColumnName");

     // So, values from "Column2" will now go into MERGEFIELDs named "Column3" as well as "Column2", if there are any
     mappedDataFields.add("Column3", "Column2");

     // The MERGEFIELD name is the "key" to the respective data source column name "value"
     Assert.assertEquals(mappedDataFields.get("MergeFieldName"), "DataSourceColumnName");
     Assert.assertTrue(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertTrue(mappedDataFields.containsValue("DataSourceColumnName"));

     // Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table
     doc.getMailMerge().execute(dataTable);

     // We can count and iterate over the mapped columns/fields
     Assert.assertEquals(mappedDataFields.getCount(), 2);

     Iterator> enumerator = mappedDataFields.iterator();
     try {
         while (enumerator.hasNext()) {
             Map.Entry dataField = enumerator.next();
             System.out.println(MessageFormat.format("Column named {0} is mapped to MERGEFIELDs named {1}", dataField.getValue(), dataField.getKey()));
         }
     } finally {
         if (enumerator != null) enumerator.remove();
     }

     // We can also remove some or all of the elements
     mappedDataFields.remove("MergeFieldName");
     Assert.assertFalse(mappedDataFields.containsKey("MergeFieldName"));
     Assert.assertFalse(mappedDataFields.containsValue("DataSourceColumnName"));

     mappedDataFields.clear();
     Assert.assertEquals(mappedDataFields.getCount(), 0);

     // Removing the mapped key/value pairs has no effect on the document because the merge was already done with them in place
     doc.save(getArtifactsDir() + "MailMerge.MappedDataFieldCollection.docx");
 }

 /// 
 /// Create a document with 2 MERGEFIELDs, one of which does not have a corresponding column in the data table.
 /// 
 private static Document createSourceDocMappedDataFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert two MERGEFIELDs that will accept data from that table
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column3");

     return doc;
 }

 /// 
 /// Create a data table with 2 columns, one of which does not have a corresponding MERGEFIELD in our source document.
 /// 
 private static DataTable createSourceTableMappedDataFields() {
     // Create a data table that will be used in a mail merge
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value1", "Value2");

     return dataTable;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| значение | java.lang.String | Имя поля в источнике данных, связанное с указанным полем слияния почты. |

