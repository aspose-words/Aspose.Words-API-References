---
title: "MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words para Java"
description: "Permite mapear automáticamente entre los nombres de los campos en su fuente de datos y los nombres de los campos de combinación de correspondencia en el documento en Java."
type: docs
weight: 448
url: /es/java/com.aspose.words/mappeddatafieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Permite mapear automáticamente entre los nombres de los campos en su fuente de datos y los nombres de los campos de mail merge en el documento.

Para obtener más información, visite el artículo de documentación [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Esto se implementa como una colección de claves de cadena a valores de cadena. Las claves son los nombres de los campos de combinación de correspondencia en el documento y los valores son los nombres de los campos en su fuente de datos.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String) | Agrega un nuevo mapeo de campo. |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String) | Determina si existe un mapeo del campo especificado en el documento dentro de la colección. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String) | Determina si existe un mapeo del campo especificado en la fuente de datos dentro de la colección. |
| [get(String documentFieldName)](#get-java.lang.String) | Obtiene el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [iterator()](#iterator) | Devuelve un objeto iterador de diccionario que puede usarse para iterar sobre todos los elementos de la colección. |
| [remove(String documentFieldName)](#remove-java.lang.String) | Elimina un mapeo de campo. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String) | Establece el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Agrega un nuevo mapeo de campo.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nombre sensible a mayúsculas y minúsculas del campo de combinación de correspondencia en el documento. |
| dataSourceFieldName | java.lang.String | Nombre sensible a mayúsculas y minúsculas del campo en la fuente de datos. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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


Determina si existe un mapeo del campo especificado en el documento dentro de la colección.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nombre sensible a mayúsculas y minúsculas del campo de combinación de correspondencia en el documento. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String}
```
public boolean containsValue(String dataSourceFieldName)
```


Determina si existe un mapeo del campo especificado en la fuente de datos dentro de la colección.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Nombre sensible a mayúsculas y minúsculas del campo en la fuente de datos. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### get(String documentFieldName) {#get-java.lang.String}
```
public String get(String documentFieldName)
```


Obtiene el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Returns:**
java.lang.String - El nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
int - El número de elementos contenidos en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador de diccionario que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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


Elimina un mapeo de campo.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nombre sensible a mayúsculas y minúsculas del campo de combinación de correspondencia en el documento. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String documentFieldName, String value)
```


Establece el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado.

 **Examples:** 

Muestra cómo mapear columnas de datos y MERGEFIELDs con nombres diferentes para que los datos se transfieran entre ellos durante una combinación de correspondencia.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| valor | java.lang.String | El nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |

