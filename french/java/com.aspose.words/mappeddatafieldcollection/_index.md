---
title: "MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words pour Java"
description: "Permet de mapper automatiquement entre les noms des champs de votre source de données et les noms des champs de publipostage dans le document en Java."
type: docs
weight: 448
url: /fr/java/com.aspose.words/mappeddatafieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Permet de mapper automatiquement les noms des champs de votre source de données aux noms des champs de fusion de courrier dans le document.

Pour en savoir plus, consultez l’article de documentation [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Ceci est implémenté comme une collection de clés de chaîne vers des valeurs de chaîne. Les clés sont les noms des champs de publipostage dans le document et les valeurs sont les noms des champs de votre source de données.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String) | Ajoute un nouveau mappage de champ. |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String) | Détermine si un mappage du champ spécifié dans le document existe dans la collection. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String) | Détermine si un mappage du champ spécifié dans la source de données existe dans la collection. |
| [get(String documentFieldName)](#get-java.lang.String) | Obtient le nom du champ dans la source de données associé au champ de publipostage spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [iterator()](#iterator) | Renvoie un objet itérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [remove(String documentFieldName)](#remove-java.lang.String) | Supprime un mappage de champ. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String) | Définit le nom du champ dans la source de données associé au champ de publipostage spécifié. |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Ajoute un nouveau mappage de champ.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nom sensible à la casse du champ de fusion dans le document. |
| dataSourceFieldName | java.lang.String | Nom sensible à la casse du champ dans la source de données. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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


Détermine si un mappage du champ spécifié dans le document existe dans la collection.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nom sensible à la casse du champ de fusion dans le document. |

**Returns:**
booléen -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String}
```
public boolean containsValue(String dataSourceFieldName)
```


Détermine si un mappage du champ spécifié dans la source de données existe dans la collection.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Nom sensible à la casse du champ dans la source de données. |

**Returns:**
booléen -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(String documentFieldName) {#get-java.lang.String}
```
public String get(String documentFieldName)
```


Obtient le nom du champ dans la source de données associé au champ de publipostage spécifié.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Returns:**
java.lang.String - Le nom du champ dans la source de données associé au champ de fusion spécifié.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
int - Le nombre d'éléments contenus dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet itérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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


Supprime un mappage de champ.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Nom sensible à la casse du champ de fusion dans le document. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String documentFieldName, String value)
```


Définit le nom du champ dans la source de données associé au champ de publipostage spécifié.

 **Examples:** 

Montre comment mapper les colonnes de données et les MERGEFIELDs avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| valeur | java.lang.String | Le nom du champ dans la source de données associé au champ de fusion spécifié. |

