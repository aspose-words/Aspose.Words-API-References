---
title: MappedDataFieldCollection
linktitle: MappedDataFieldCollection
second_title: Aspose.Words for Java
description: Allows to automatically map between names of fields in your data source and names of mail merge fields in the document in Java.
type: docs
weight: 441
url: /java/com.aspose.words/mappeddatafieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
## Methods

| Method | Description |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String) | Adds a new field mapping. |
| [clear()](#clear) | Removes all elements from the collection. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [get(String documentFieldName)](#get-java.lang.String) | Gets the name of the field in the data source associated with the specified mail merge field. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [iterator()](#iterator) | Returns a dictionary iterator object that can be used to iterate over all items in the collection. |
| [remove(String documentFieldName)](#remove-java.lang.String) | Removes a field mapping. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String) | Sets the name of the field in the data source associated with the specified mail merge field. |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Adds a new field mapping.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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


Determines whether a mapping from the specified field in the document exists in the collection.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

**Returns:**
boolean -  true  if item is found in the collection; otherwise,  false .
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String}
```
public boolean containsValue(String dataSourceFieldName)
```


Determines whether a mapping from the specified field in the data source exists in the collection.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

**Returns:**
boolean -  true  if item is found in the collection; otherwise,  false .
### get(String documentFieldName) {#get-java.lang.String}
```
public String get(String documentFieldName)
```


Gets the name of the field in the data source associated with the specified mail merge field.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Returns:**
java.lang.String - The name of the field in the data source associated with the specified mail merge field.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
int - The number of elements contained in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns a dictionary iterator object that can be used to iterate over all items in the collection.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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


Removes a field mapping.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String documentFieldName, String value)
```


Sets the name of the field in the data source associated with the specified mail merge field.

 **Examples:** 

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

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
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| value | java.lang.String | The name of the field in the data source associated with the specified mail merge field. |

