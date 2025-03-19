---
title: MailMerge
linktitle: MailMerge
second_title: Aspose.Words for Java
description: Represents the mail merge functionality in Java.
type: docs
weight: 427
url: /java/com.aspose.words/mailmerge/
---

**Inheritance:**
java.lang.Object
```
public class MailMerge
```

Represents the mail merge functionality.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

For mail merge operation to work, the document should contain Word MERGEFIELD and optionally NEXT fields. During mail merge operation, merge fields in the document are replaced with values from your data source.

There are two distinct ways to use mail merge: with mail merge regions and without.

The simplest mail merge is without regions and it is very similar to how mail merge works in Word. Use  Execute  methods to merge information from some data source such as **DataTable**, **DataSet** or an array of objects into your document. The [MailMerge](../../com.aspose.words/mailmerge/) object processes all records of the data source and copies and appends content of the whole document for each record.

Note that when [MailMerge](../../com.aspose.words/mailmerge/) object encounters a NEXT field, it selects next record in the data source and continues merging without copying any content.

Use [executeWithRegions(com.aspose.words.IMailMergeDataSource)](../../com.aspose.words/mailmerge/\#executeWithRegions-com.aspose.words.IMailMergeDataSource) and other overloads to merge information into a document with mail merge regions defined. You can use **DataTable** or **DataSet** as data sources for this operation.

You need to use mail merge regions if you want to dynamically grow portions inside the document. Without mail merge regions whole document will be repeated for every record of the data source.

 **Examples:** 

Shows how to execute a mail merge with data from a DataTable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // This example creates a table, but you would normally load table from a database
 DataTable table = new DataTable("Test");
 table.getColumns().add("CustomerName");
 table.getColumns().add("Address");
 table.getRows().add("Thomas Hardy", "120 Hanover Sq., London");
 table.getRows().add("Paolo Accorti", "Via Monte Bianco 34, Torino");

 // Field values from the table are inserted into the mail merge fields found in the document
 doc.getMailMerge().execute(table);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.docx");

 // Create a copy of our document to perform another mail merge
 doc = new Document();
 builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // We can also source values for a mail merge from a single row in the table
 doc.getMailMerge().execute(table.getRows().get(1));

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.OneRow.docx");
 
```


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [deleteFields()](#deleteFields) | Removes mail merge related fields from the document. |
| [execute(IMailMergeDataSource dataSource)](#execute-com.aspose.words.IMailMergeDataSource) | Performs a mail merge from a custom data source. |
| [execute(System.Data.DataRow row)](#execute-com.aspose.words.net.System.Data.DataRow) | Performs mail merge from a **DataRow** into the document. |
| [execute(System.Data.DataTable table)](#execute-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a com.aspose.words.net.System.Data.DataTable into the document. |
| [execute(System.Data.DataView dataView)](#execute-com.aspose.words.net.System.Data.DataView) | Performs mail merge from a **DataView** into the document. |
| [execute(System.Data.IDataReader dataReader)](#execute-com.aspose.words.net.System.Data.IDataReader) | Performs mail merge from **IDataReader** into the document. |
| [execute(String[] fieldNames, Object[] values)](#execute-java.lang.String---java.lang.Object) | Performs a mail merge operation. |
| [executeWithRegions(IMailMergeDataSource dataSource)](#executeWithRegions-com.aspose.words.IMailMergeDataSource) | Performs a mail merge from a custom data source with mail merge regions. |
| [executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)](#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot) | Performs a mail merge from a custom data source with mail merge regions. |
| [executeWithRegions(System.Data.DataSet dataSet)](#executeWithRegions-com.aspose.words.net.System.Data.DataSet) | Performs a mail merge operation into a document with mail merge regions. |
| [executeWithRegions(System.Data.DataTable dataTable)](#executeWithRegions-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a **DataTable** into the document with mail merge regions. |
| [executeWithRegions(System.Data.DataView dataView)](#executeWithRegions-com.aspose.words.net.System.Data.DataView) | Performs mail merge from a **DataView** into the document with mail merge regions. |
| [executeWithRegions(System.Data.IDataReader dataReader, String tableName)](#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String) | Performs mail merge from **IDataReader** into the document with mail merge regions. |
| [getCleanupOptions()](#getCleanupOptions) | Gets a set of flags that specify what items should be removed during mail merge. |
| [getCleanupParagraphsWithPunctuationMarks()](#getCleanupParagraphsWithPunctuationMarks) | Gets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |
| [getFieldMergingCallback()](#getFieldMergingCallback) | Occurs during mail merge when a mail merge field is encountered in the document. |
| [getFieldNames()](#getFieldNames) | Returns a collection of mail merge field names available in the document. |
| [getFieldNamesForRegion(String regionName)](#getFieldNamesForRegion-java.lang.String) | Get mail merge field names from the region. |
| [getFieldNamesForRegion(String regionName, int regionIndex)](#getFieldNamesForRegion-java.lang.String-int) | Returns a collection of mail merge field names available in the region. |
| [getMailMergeCallback()](#getMailMergeCallback) | Allows to handle particular events during mail merge. |
| [getMappedDataFields()](#getMappedDataFields) | Returns a collection that represents mapped data fields for the mail merge operation. |
| [getMergeDuplicateRegions()](#getMergeDuplicateRegions) | Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [getMergeWholeDocument()](#getMergeWholeDocument) | Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [getPreserveUnusedTags()](#getPreserveUnusedTags) | Gets a value indicating whether the unused "mustache" tags should be preserved. |
| [getRegionEndTag()](#getRegionEndTag) | Gets a mail merge region end tag. |
| [getRegionStartTag()](#getRegionStartTag) | Gets a mail merge region start tag. |
| [getRegionsByName(String regionName)](#getRegionsByName-java.lang.String) | Returns a collection of mail merge regions with the specified name. |
| [getRegionsHierarchy()](#getRegionsHierarchy) | Returns a full hierarchy of regions (with fields) available in the document. |
| [getRestartListsAtEachSection()](#getRestartListsAtEachSection) | Gets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [getRetainFirstSectionStart()](#getRetainFirstSectionStart) | Gets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [getTrimWhitespaces()](#getTrimWhitespaces) | Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [getUnconditionalMergeFieldsAndRegions()](#getUnconditionalMergeFieldsAndRegions) | Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [getUseNonMergeFields()](#getUseNonMergeFields) | When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags. |
| [getUseWholeParagraphAsRegion()](#getUseWholeParagraphAsRegion) | Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
| [setCleanupOptions(int value)](#setCleanupOptions-int) | Sets a set of flags that specify what items should be removed during mail merge. |
| [setCleanupParagraphsWithPunctuationMarks(boolean value)](#setCleanupParagraphsWithPunctuationMarks-boolean) | Sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |
| [setFieldMergingCallback(IFieldMergingCallback value)](#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback) | Occurs during mail merge when a mail merge field is encountered in the document. |
| [setMailMergeCallback(IMailMergeCallback value)](#setMailMergeCallback-com.aspose.words.IMailMergeCallback) | Allows to handle particular events during mail merge. |
| [setMergeDuplicateRegions(boolean value)](#setMergeDuplicateRegions-boolean) | Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [setMergeWholeDocument(boolean value)](#setMergeWholeDocument-boolean) | Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [setPreserveUnusedTags(boolean value)](#setPreserveUnusedTags-boolean) | Sets a value indicating whether the unused "mustache" tags should be preserved. |
| [setRegionEndTag(String value)](#setRegionEndTag-java.lang.String) | Sets a mail merge region end tag. |
| [setRegionStartTag(String value)](#setRegionStartTag-java.lang.String) | Sets a mail merge region start tag. |
| [setRestartListsAtEachSection(boolean value)](#setRestartListsAtEachSection-boolean) | Sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [setRetainFirstSectionStart(boolean value)](#setRetainFirstSectionStart-boolean) | Sets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [setTrimWhitespaces(boolean value)](#setTrimWhitespaces-boolean) | Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [setUnconditionalMergeFieldsAndRegions(boolean value)](#setUnconditionalMergeFieldsAndRegions-boolean) | Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [setUseNonMergeFields(boolean value)](#setUseNonMergeFields-boolean) | When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags. |
| [setUseWholeParagraphAsRegion(boolean value)](#setUseWholeParagraphAsRegion-boolean) | Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
### deleteFields() {#deleteFields}
```
public void deleteFields()
```


Removes mail merge related fields from the document.

 **Remarks:** 

This method removes MERGEFIELD and NEXT fields from the document.

This method could be useful if your mail merge operation does not always need to populate all fields in the document. Use this method to remove all remaining mail merge fields.

 **Examples:** 

Shows how to delete all merge fields from a document without executing mail merge.

```

 doc.getMailMerge().deleteFields();
 
```

### execute(IMailMergeDataSource dataSource) {#execute-com.aspose.words.IMailMergeDataSource}
```
public void execute(IMailMergeDataSource dataSource)
```


Performs a mail merge from a custom data source.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from any data source such as a list or hashtable or objects. You need to write your own class that implements the [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) interface.

You can use this method only when [FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate-boolean) is  false , that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

 **Examples:** 

Shows how to execute a mail merge with a data source in the form of a custom object.

```

 public void customDataSource() throws Exception {
     // Create a destination document for the mail merge
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(" MERGEFIELD FullName ");
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD Address ");

     // Create some data that we will use in the mail merge
     CustomerList customers = new CustomerList();
     customers.add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
     customers.add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // To be able to mail merge from your own data source, it must be wrapped
     // into an object that implements the IMailMergeDataSource interface
     CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

     // Now you can pass your data source into Aspose.Words
     doc.getMailMerge().execute(customersDataSource);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSource.docx");
 }

 // An example of a "data entity" class in your application.
 public class Customer {
     public Customer(final String aFullName, final String anAddress) {
         mFullName = aFullName;
         mAddress = anAddress;
     }

     public String getFullName() {
         return mFullName;
     }

     public void setFullName(final String value) {
         mFullName = value;
     }

     public String getAddress() {
         return mAddress;
     }

     public void setAddress(final String value) {
         mAddress = value;
     }

     private String mFullName;
     private String mAddress;
 }

 // An example of a typed collection that contains your "data" objects.
 public class CustomerList extends ArrayList {
     public Customer get(final int index) {
         return (Customer) super.get(index);
     }

     public void set(final int index, final Customer value) {
         super.set(index, value);
     }
 }

 // A custom mail merge data source that you implement to allow Aspose.Words
 // to mail merge data from your Customer objects into Microsoft Word documents.
 public class CustomerMailMergeDataSource implements IMailMergeDataSource {
     public CustomerMailMergeDataSource(final CustomerList customers) {
         mCustomers = customers;

         // When the data source is initialized, it must be positioned before the first record.
         mRecordIndex = -1;
     }

     // The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     public String getTableName() {
         return "Customer";
     }

     // Aspose.Words calls this method to get a value for every data field.
     public boolean getValue(final String fieldName, final Ref fieldValue) throws Exception {
         if (fieldName.equals("FullName")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getFullName());
             return true;
         } else if (fieldName.equals("Address")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getAddress());
             return true;
         } else {
             // A field with this name was not found,
             // return false to the Aspose.Words mail merge engine
             fieldValue.set(null);
             return false;
         }
     }

     // A standard implementation for moving to a next record in a collection.
     public boolean moveNext() {
         if (!isEof()) mRecordIndex++;

         return (!isEof());
     }

     public IMailMergeDataSource getChildDataSource(final String tableName) {
         return null;
     }

     private boolean isEof() {
         return (mRecordIndex >= mCustomers.size());
     }

     private final CustomerList mCustomers;
     private int mRecordIndex;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### execute(System.Data.DataRow row) {#execute-com.aspose.words.net.System.Data.DataRow}
```
public void execute(System.Data.DataRow row)
```


Performs mail merge from a **DataRow** into the document.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from a **DataRow**.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

 **Examples:** 

Shows how to execute a mail merge with data from a DataTable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // This example creates a table, but you would normally load table from a database
 DataTable table = new DataTable("Test");
 table.getColumns().add("CustomerName");
 table.getColumns().add("Address");
 table.getRows().add("Thomas Hardy", "120 Hanover Sq., London");
 table.getRows().add("Paolo Accorti", "Via Monte Bianco 34, Torino");

 // Field values from the table are inserted into the mail merge fields found in the document
 doc.getMailMerge().execute(table);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.docx");

 // Create a copy of our document to perform another mail merge
 doc = new Document();
 builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // We can also source values for a mail merge from a single row in the table
 doc.getMailMerge().execute(table.getRows().get(1));

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.OneRow.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(System.Data.DataTable table) {#execute-com.aspose.words.net.System.Data.DataTable}
```
public void execute(System.Data.DataTable table)
```


Performs mail merge from a com.aspose.words.net.System.Data.DataTable into the document.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from a **DataTable**.

All records from the table are merged into the document.

You can use NEXT field in the Word document to cause [MailMerge](../../com.aspose.words/mailmerge/) object to select next record from the **DataTable** and continue merging. This can be used when creating documents such as mailing labels.

When [MailMerge](../../com.aspose.words/mailmerge/) object reaches end of the main document and there are still more rows in the **DataTable**, it copies entire content of the main document and appends it to the end of the destination document using a section break as a separator.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

 **Examples:** 

Shows how to execute a mail merge with data from a DataTable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // This example creates a table, but you would normally load table from a database
 DataTable table = new DataTable("Test");
 table.getColumns().add("CustomerName");
 table.getColumns().add("Address");
 table.getRows().add("Thomas Hardy", "120 Hanover Sq., London");
 table.getRows().add("Paolo Accorti", "Via Monte Bianco 34, Torino");

 // Field values from the table are inserted into the mail merge fields found in the document
 doc.getMailMerge().execute(table);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.docx");

 // Create a copy of our document to perform another mail merge
 doc = new Document();
 builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // We can also source values for a mail merge from a single row in the table
 doc.getMailMerge().execute(table.getRows().get(1));

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.OneRow.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(System.Data.DataView dataView) {#execute-com.aspose.words.net.System.Data.DataView}
```
public void execute(System.Data.DataView dataView)
```


Performs mail merge from a **DataView** into the document.

 **Remarks:** 

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview/) | Data source for the mail merge operation. |

### execute(System.Data.IDataReader dataReader) {#execute-com.aspose.words.net.System.Data.IDataReader}
```
public void execute(System.Data.IDataReader dataReader)
```


Performs mail merge from **IDataReader** into the document.

 **Remarks:** 

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

 **Examples:** 

Shows how to run a mail merge using data from a data reader.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Product:\t");
 builder.insertField(" MERGEFIELD ProductName");
 builder.write("\nSupplier:\t");
 builder.insertField(" MERGEFIELD CompanyName");
 builder.writeln();
 builder.insertField(" MERGEFIELD QuantityPerUnit");
 builder.write(" for $");
 builder.insertField(" MERGEFIELD UnitPrice");

 // "DocumentHelper.executeDataTable" is utility function that creates a connection, command,
 // executes the command and return the result in a DataTable.
 ResultSet resultSet = DocumentHelper.executeDataTable(
         "SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, " +
                 "{fn ROUND(Products.UnitPrice,2)} as UnitPrice " +
                 "FROM Products INNER JOIN Suppliers ON Products.SupplierID = Suppliers.SupplierID");
 DataTable dataTable = new DataTable(resultSet, "OrderDetails");
 IDataReader dataReader = new DataTableReader(dataTable);

 // Now we can take the data from the reader and use it in the mail merge.
 doc.getMailMerge().execute(dataReader);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataReader.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) | Data source for the mail merge operation. |

### execute(String[] fieldNames, Object[] values) {#execute-java.lang.String---java.lang.Object}
```
public void execute(String[] fieldNames, Object[] values)
```


Performs a mail merge operation.  Performs a mail merge operation for a single record.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from an array of objects.

This method merges data for one record only. The array of field names and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

 **Examples:** 

Demonstrates how to merge an image from a web address using an Image field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD  Image:Logo ");

 // Pass a URL which points to the image to merge into the document
 doc.getMailMerge().execute(new String[]{"Logo"}, new Object[]{DocumentHelper.getBytesFromStream(getAsposelogoUri().toURL().openStream())});

 doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromUrl.doc");
 
```

Shows how to perform a mail merge, and then save the document to the client browser.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| values | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in  fieldNames . |

### executeWithRegions(IMailMergeDataSource dataSource) {#executeWithRegions-com.aspose.words.IMailMergeDataSource}
```
public void executeWithRegions(IMailMergeDataSource dataSource)
```


Performs a mail merge from a custom data source with mail merge regions.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own class that implements the [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) interface.

You can use this method only when [FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate-boolean) is  false , that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot) {#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot}
```
public void executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```


Performs a mail merge from a custom data source with mail merge regions.

 **Remarks:** 

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own classes that implement the [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot/) and [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) interfaces.

You can use this method only when [FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate-boolean) is  false , that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

 **Examples:** 

Performs mail merge from a custom data source with master-detail data.

```

 public void customDataSourceRoot() throws Exception {
     // Create a document with two mail merge regions named "Washington" and "Seattle"
     Document doc = createSourceDocumentWithMailMergeRegions(new String[]{"Washington", "Seattle"});

     // Create two data sources
     EmployeeList employeesWashingtonBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Doe", "Sales"));
     employeesWashingtonBranch.add(new Employee("Jane Doe", "Management"));

     EmployeeList employeesSeattleBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Cardholder", "Management"));
     employeesWashingtonBranch.add(new Employee("Joe Bloggs", "Sales"));

     // Register our data sources by name in a data source root
     DataSourceRoot sourceRoot = new DataSourceRoot();
     sourceRoot.registerSource("Washington", new EmployeeListMailMergeSource(employeesWashingtonBranch));
     sourceRoot.registerSource("Seattle", new EmployeeListMailMergeSource(employeesSeattleBranch));

     // Since we have consecutive mail merge regions, we would normally have to perform two mail merges
     // However, one mail merge source data root call every relevant data source and merge automatically
     doc.getMailMerge().executeWithRegions(sourceRoot);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSourceRoot.docx");
 }

 /// 
 /// Create document that contains consecutive mail merge regions, with names designated by the input array,
 /// for a data table of employees.
 /// 
 private static Document createSourceDocumentWithMailMergeRegions(String[] regions) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (String s : regions) {
         builder.writeln("\n" + s + " branch: ");
         builder.insertField(" MERGEFIELD TableStart:" + s);
         builder.insertField(" MERGEFIELD FullName");
         builder.write(", ");
         builder.insertField(" MERGEFIELD Department");
         builder.insertField(" MERGEFIELD TableEnd:" + s);
     }

     return doc;
 }

 /// 
 /// An example of a "data entity" class in your application.
 /// 
 private static class Employee {
     public Employee(String aFullName, String aDepartment) {
         mFullName = aFullName;
         mDepartment = aDepartment;
     }

     public String getFullName() {
         return mFullName;
     }

     private final String mFullName;

     public String getDepartment() {
         return mDepartment;
     }

     private final String mDepartment;
 }

 /// 
 /// An example of a typed collection that contains your "data" objects.
 /// 
 private static class EmployeeList extends ArrayList {
     public Employee get(int index) {
         return (Employee) super.get(index);
     }

     public void set(int index, Employee value) {
         super.set(index, value);
     }
 }

 /// 
 /// Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
 /// These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
 /// which corresponds to a mail merge region that will read the respective data.
 /// 
 private static class DataSourceRoot implements IMailMergeDataSourceRoot {
     public IMailMergeDataSource getDataSource(String tableName) {
         EmployeeListMailMergeSource source = mSources.get(tableName);
         source.reset();
         return mSources.get(tableName);
     }

     public void registerSource(String sourceName, EmployeeListMailMergeSource source) {
         mSources.put(sourceName, source);
     }

     private final HashMap mSources = new HashMap<>();
 }

 /// 
 /// Custom mail merge data source.
 /// 
 private static class EmployeeListMailMergeSource implements IMailMergeDataSource {
     public EmployeeListMailMergeSource(EmployeeList employees) {
         mEmployees = employees;
         mRecordIndex = -1;
     }

     /// 
     /// A standard implementation for moving to a next record in a collection.
     /// 
     public boolean moveNext() {
         if (!isEof())
             mRecordIndex++;

         return (!isEof());
     }

     private boolean isEof() {
         return (mRecordIndex >= mEmployees.size());
     }

     public void reset() {
         mRecordIndex = -1;
     }

     /// 
     /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     /// 
     public String getTableName() {
         return "Employees";
     }

     /// 
     /// Aspose.Words calls this method to get a value for every data field.
     /// 
     public boolean getValue(String fieldName, Ref fieldValue) {
         switch (fieldName) {
             case "FullName":
                 fieldValue.set(mEmployees.get(mRecordIndex).getFullName());
                 return true;
             case "Department":
                 fieldValue.set(mEmployees.get(mRecordIndex).getDepartment());
                 return true;
             default:
                 // A field with this name was not found,
                 // return false to the Aspose.Words mail merge engine
                 fieldValue.set(null);
                 return false;
         }
     }

     /// 
     /// Child data sources are for nested mail merges.
     /// 
     public IMailMergeDataSource getChildDataSource(String tableName) {
         throw new UnsupportedOperationException();
     }

     private final EmployeeList mEmployees;
     private int mRecordIndex;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceRoot | [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot/) | An object that implements the custom mail merge data source root interface. |

### executeWithRegions(System.Data.DataSet dataSet) {#executeWithRegions-com.aspose.words.net.System.Data.DataSet}
```
public void executeWithRegions(System.Data.DataSet dataSet)
```


Performs a mail merge operation into a document with mail merge regions. Supports parent-child (master-detail) data sources and nested mail merge regions.  Performs mail merge from a **DataSet** into a document with mail merge regions.

 **Remarks:** 

Use this method to perform mail merge from one or more tables into repeatable mail merge regions in the document. The mail merge regions inside the document will dynamically grow to accommodate records in the corresponding tables.

The document must have mail merge regions defined with names that refer to the tables in the **DataSet**.

To specify a mail merge region in the document you need to insert two mail merge fields to mark beginning and end of the mail merge region.

All document content that is included inside a mail merge region will be automatically repeated for every record in the **DataTable**.

To mark beginning of a mail merge region insert a MERGEFIELD with name TableStart:MyTable, where MyTable corresponds to one of the table names in your **DataSet**.

To mark the end of the mail merge region insert another MERGEFIELD with name TableEnd:MyTable.

To insert a MERGEFIELD in Word use Insert/Field command and select MergeField then type the name of the field.

The **TableStart** and **TableEnd** fields must be inside the same section in your document.

If used inside a table, **TableStart** and **TableEnd** must be inside the same row in the table.

Mail merge regions in a document should be well formed (there always needs to be a pair of matching **TableStart** and **TableEnd** merge fields with the same table name).

 **Examples:** 

Shows how to execute a nested mail merge with two merge regions and two data tables.

```

 public void executeWithRegionsNested() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
     // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
     // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
     builder.insertField(" MERGEFIELD TableStart:Customers");

     // This MERGEFIELD is inside the mail merge region of the "Customers" table.
     // When we execute the mail merge, this field will receive data from rows in a data source named "Customers".
     builder.write("Orders for ");
     builder.insertField(" MERGEFIELD CustomerName");
     builder.write(":");

     // Create column headers for a table that will contain values from a second inner region.
     builder.startTable();
     builder.insertCell();
     builder.write("Item");
     builder.insertCell();
     builder.write("Quantity");
     builder.endRow();

     // Create a second mail merge region inside the outer region for a table named "Orders".
     // The "Orders" table has a many-to-one relationship with the "Customers" table on the "CustomerID" column.
     builder.insertCell();
     builder.insertField(" MERGEFIELD TableStart:Orders");
     builder.insertField(" MERGEFIELD ItemName");
     builder.insertCell();
     builder.insertField(" MERGEFIELD Quantity");

     // End the inner region
     // One stipulation of using regions and tables is that the opening and closing of a mail merge region must
     // only happen over one row of a document's table
     builder.insertField(" MERGEFIELD TableEnd:Orders");
     builder.endTable();

     builder.insertField(" MERGEFIELD TableEnd:Customers");

     // Create a dataset that contains the two tables with the required names and relationships.
     // Each merge document for each row of the "Customers" table of the outer merge region will perform its mail merge on the "Orders" table.
     // Each merge document will display all rows of the latter table whose "CustomerID" column values match the current "Customers" table row.
     DataSet customersAndOrders = createDataSet();
     doc.getMailMerge().executeWithRegions(customersAndOrders);

     doc.save(getArtifactsDir() + "MailMerge.ExecuteWithRegionsNested.docx");
 }

 /// 
 /// Generates a data set which has two data tables named "Customers" and "Orders",
 /// with a one-to-many relationship between the former and latter on the "CustomerID" column.
 /// 
 private static DataSet createDataSet() {
     // Create the outer mail merge
     DataTable tableCustomers = new DataTable("Customers");
     tableCustomers.getColumns().add("CustomerID");
     tableCustomers.getColumns().add("CustomerName");
     tableCustomers.getRows().add(1, "John Doe");
     tableCustomers.getRows().add(2, "Jane Doe");

     // Create the table for the inner merge
     DataTable tableOrders = new DataTable("Orders");
     tableOrders.getColumns().add("CustomerID");
     tableOrders.getColumns().add("ItemName");
     tableOrders.getColumns().add("Quantity");
     tableOrders.getRows().add(1, "Hawaiian", 2);
     tableOrders.getRows().add(2, "Pepperoni", 1);
     tableOrders.getRows().add(2, "Chicago", 1);

     // Add both tables to a data set
     DataSet dataSet = new DataSet();
     dataSet.getTables().add(tableCustomers);
     dataSet.getTables().add(tableOrders);

     // The "CustomerID" column, also the primary key of the customers table is the foreign key for the Orders table
     dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

     return dataSet;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | **DataSet** that contains data to be inserted into mail merge fields. |

### executeWithRegions(System.Data.DataTable dataTable) {#executeWithRegions-com.aspose.words.net.System.Data.DataTable}
```
public void executeWithRegions(System.Data.DataTable dataTable)
```


Performs mail merge from a **DataTable** into the document with mail merge regions.

 **Remarks:** 

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

 **Examples:** 

Shows how to use regions to execute two separate mail merges in one document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we want to perform two consecutive mail merges on one document while taking data from two tables
 // related to each other in any way, we can separate the mail merges with regions.
 // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
 // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
 // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
 // These regions are separate for unrelated data, while they can be nested for hierarchical data.
 builder.writeln("\tCities: ");
 builder.insertField(" MERGEFIELD TableStart:Cities");
 builder.insertField(" MERGEFIELD Name");
 builder.insertField(" MERGEFIELD TableEnd:Cities");
 builder.insertParagraph();

 // Both MERGEFIELDs refer to the same column name, but values for each will come from different data tables.
 builder.writeln("\tFruit: ");
 builder.insertField(" MERGEFIELD TableStart:Fruit");
 builder.insertField(" MERGEFIELD Name");
 builder.insertField(" MERGEFIELD TableEnd:Fruit");

 // Create two unrelated data tables.
 DataTable tableCities = new DataTable("Cities");
 tableCities.getColumns().add("Name");
 tableCities.getRows().add("Washington");
 tableCities.getRows().add("London");
 tableCities.getRows().add("New York");

 DataTable tableFruit = new DataTable("Fruit");
 tableFruit.getColumns().add("Name");
 tableFruit.getRows().add("Cherry");
 tableFruit.getRows().add("Apple");
 tableFruit.getRows().add("Watermelon");
 tableFruit.getRows().add("Banana");

 // We will need to run one mail merge per table. The first mail merge will populate the MERGEFIELDs
 // in the "Cities" range while leaving the fields the "Fruit" range unfilled.
 doc.getMailMerge().executeWithRegions(tableCities);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteWithRegionsConcurrent.docx");
 
```

Demonstrates how to implement custom logic in the MergeField event to apply cell formatting.

```

 public void alternatingRows() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind suppliers.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldAlternatingRows());

     // Execute mail merge with regions
     DataTable dataTable = getSuppliersDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     doc.save(getArtifactsDir() + "MailMergeEvent.AlternatingRows.docx");
 }

 private class HandleMergeFieldAlternatingRows implements IFieldMergingCallback {
     // Called for every merge field encountered in the document.
     // We can either return some data to the mail merge engine or do something
     // else with the document. In this case we modify cell formatting.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (mBuilder == null) {
             mBuilder = new DocumentBuilder(args.getDocument());
         }

         // This way we catch the beginning of a new row
         if (args.getFieldName().equals("CompanyName")) {
             // Select the color depending on whether the row number is even or odd
             Color rowColor;
             if (isOdd(mRowIdx)) rowColor = new Color(213, 227, 235);
             else rowColor = new Color(242, 242, 242);

             // There is no way to set cell properties for the whole row at the moment,
             // so we have to iterate over all cells in the row
             for (int colIdx = 0; colIdx < 4; colIdx++) {
                 mBuilder.moveToCell(0, mRowIdx, colIdx, 0);
                 mBuilder.getCellFormat().getShading().setBackgroundPatternColor(rowColor);
             }

             mRowIdx++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     private DocumentBuilder mBuilder;
     private int mRowIdx;
 }

 /*
 // Returns true if the value is odd; false if the value is even.
 /

 private static boolean isOdd(final int value) {
     return (value % 2 != 0);
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getSuppliersDataTable() throws Exception {
     DataTable dataTable = new DataTable("Suppliers");
     dataTable.getColumns().add("CompanyName");
     dataTable.getColumns().add("ContactName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Company " + i);
         datarow.set(1, "Contact " + i);
     }

     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Data source for the mail merge operation. The table must have its [DataTable.getTableName()](../../com.aspose.words.net.system.data/datatable/\#getTableName) / [DataTable.setTableName(java.lang.String)](../../com.aspose.words.net.system.data/datatable/\#setTableName-java.lang.String) property set. |

### executeWithRegions(System.Data.DataView dataView) {#executeWithRegions-com.aspose.words.net.System.Data.DataView}
```
public void executeWithRegions(System.Data.DataView dataView)
```


Performs mail merge from a **DataView** into the document with mail merge regions.

 **Remarks:** 

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

The document must have a mail merge region defined with name that matches **DataView.Table.TableName**.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

 **Examples:** 

Shows how to use regions to execute two separate mail merges in one document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we want to perform two consecutive mail merges on one document while taking data from two tables
 // related to each other in any way, we can separate the mail merges with regions.
 // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
 // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
 // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
 // These regions are separate for unrelated data, while they can be nested for hierarchical data.
 builder.writeln("\tCities: ");
 builder.insertField(" MERGEFIELD TableStart:Cities");
 builder.insertField(" MERGEFIELD Name");
 builder.insertField(" MERGEFIELD TableEnd:Cities");
 builder.insertParagraph();

 // Both MERGEFIELDs refer to the same column name, but values for each will come from different data tables.
 builder.writeln("\tFruit: ");
 builder.insertField(" MERGEFIELD TableStart:Fruit");
 builder.insertField(" MERGEFIELD Name");
 builder.insertField(" MERGEFIELD TableEnd:Fruit");

 // Create two unrelated data tables.
 DataTable tableCities = new DataTable("Cities");
 tableCities.getColumns().add("Name");
 tableCities.getRows().add("Washington");
 tableCities.getRows().add("London");
 tableCities.getRows().add("New York");

 DataTable tableFruit = new DataTable("Fruit");
 tableFruit.getColumns().add("Name");
 tableFruit.getRows().add("Cherry");
 tableFruit.getRows().add("Apple");
 tableFruit.getRows().add("Watermelon");
 tableFruit.getRows().add("Banana");

 // We will need to run one mail merge per table. The first mail merge will populate the MERGEFIELDs
 // in the "Cities" range while leaving the fields the "Fruit" range unfilled.
 doc.getMailMerge().executeWithRegions(tableCities);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteWithRegionsConcurrent.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview/) | Data source for the mail merge operation. The source table of the **DataView** must have its **TableName** property set. |

### executeWithRegions(System.Data.IDataReader dataReader, String tableName) {#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String}
```
public void executeWithRegions(System.Data.IDataReader dataReader, String tableName)
```


Performs mail merge from **IDataReader** into the document with mail merge regions.

 **Remarks:** 

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

 **Examples:** 

Shows how to insert images stored in a database BLOB field into a report.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) | Source of the data records for mail merge such as **OleDbDataReader** or **SqlDataReader**. |
| tableName | java.lang.String | Name of the mail merge region in the document to populate. |

### getCleanupOptions() {#getCleanupOptions}
```
public int getCleanupOptions()
```


Gets a set of flags that specify what items should be removed during mail merge.

 **Examples:** 

Shows how to automatically remove unmerged merge fields during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Shows how to make sure empty paragraphs that result from merging fields with no data are removed from the document.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Shows how to instruct the mail merge engine to remove any containing fields from around a merge field during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

**Returns:**
int - A set of flags that specify what items should be removed during mail merge. The returned value is a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants.
### getCleanupParagraphsWithPunctuationMarks() {#getCleanupParagraphsWithPunctuationMarks}
```
public boolean getCleanupParagraphsWithPunctuationMarks()
```


Gets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.

 **Remarks:** 

The default value is  true .

Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

 **Examples:** 

Shows how to remove paragraphs with punctuation marks after mail merge operation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.insertField("MERGEFIELD", "Option_1");
 mergeFieldOption1.setFieldName("Option_1");

 // Here is the complete list of cleanable punctuation marks:
 // !
 // ,
 // .
 // :
 // ;
 // ?
 // ¡
 // ¿
 builder.write(punctuationMark);

 FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.insertField("MERGEFIELD", "Option_2");
 mergeFieldOption2.setFieldName("Option_2");

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 // The default value of the option is true which means that the behavior was changed to mimic MS Word
 // If you rely on the old behavior are able to revert it by setting the option to false
 doc.getMailMerge().setCleanupParagraphsWithPunctuationMarks(isCleanupParagraphsWithPunctuationMarks);

 doc.getMailMerge().execute(new String[]{"Option_1", "Option_2"}, new Object[]{null, null});

 doc.save(getArtifactsDir() + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
 
```

**Returns:**
boolean - A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.
### getFieldMergingCallback() {#getFieldMergingCallback}
```
public IFieldMergingCallback getFieldMergingCallback()
```


Occurs during mail merge when a mail merge field is encountered in the document.

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

Shows how to insert images stored in a database BLOB field into a report.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```

**Returns:**
[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) - The corresponding [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) value.
### getFieldNames() {#getFieldNames}
```
public String[] getFieldNames()
```


Returns a collection of mail merge field names available in the document.

 **Remarks:** 

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

A new string array is created on every call.

Includes "mustache" field names if [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is  true .

 **Examples:** 

Shows how to get names of all merge fields in a document.

```

 String[] fieldNames = doc.getMailMerge().getFieldNames();
 
```

**Returns:**
java.lang.String[]
### getFieldNamesForRegion(String regionName) {#getFieldNamesForRegion-java.lang.String}
```
public String[] getFieldNamesForRegion(String regionName)
```


Get mail merge field names from the region.  Returns a collection of mail merge field names available in the region.

 **Remarks:** 

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the very first region is processed.

A new string array is created on every call.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| regionName | java.lang.String | Region name (case-insensitive). |

**Returns:**
java.lang.String[]
### getFieldNamesForRegion(String regionName, int regionIndex) {#getFieldNamesForRegion-java.lang.String-int}
```
public String[] getFieldNamesForRegion(String regionName, int regionIndex)
```


Returns a collection of mail merge field names available in the region.

 **Remarks:** 

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the Nth region (zero-based) is processed.

A new string array is created on every call.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| regionName | java.lang.String | Region name (case-insensitive). |
| regionIndex | int | Region index (zero-based). |

**Returns:**
java.lang.String[]
### getMailMergeCallback() {#getMailMergeCallback}
```
public IMailMergeCallback getMailMergeCallback()
```


Allows to handle particular events during mail merge.

 **Examples:** 

Shows how to define custom logic for handling events during mail merge.

```

 public void testTagsReplacedEventShouldRisedWithUseNonMergeFieldsOption() throws Exception {
     Document document = new Document();
     document.getMailMerge().setUseNonMergeFields(true);

     MailMergeCallbackStub mailMergeCallbackStub = new MailMergeCallbackStub();
     document.getMailMerge().setMailMergeCallback(mailMergeCallbackStub);

     document.getMailMerge().execute(new String[0], new Object[0]);

     Assert.assertEquals(mailMergeCallbackStub.getTagsReplacedCounter(), 1);
 }

 private static class MailMergeCallbackStub implements IMailMergeCallback {
     public void tagsReplaced() {
         mTagsReplacedCounter++;
     }

     public int getTagsReplacedCounter() {
         return mTagsReplacedCounter;
     }

     private int mTagsReplacedCounter;
 }
 
```

**Returns:**
[IMailMergeCallback](../../com.aspose.words/imailmergecallback/) - The corresponding [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) value.
### getMappedDataFields() {#getMappedDataFields}
```
public MappedDataFieldCollection getMappedDataFields()
```


Returns a collection that represents mapped data fields for the mail merge operation.

 **Remarks:** 

Mapped data fields allow to automatically map between names of fields in your data source and names of mail merge fields in the document.

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
[MappedDataFieldCollection](../../com.aspose.words/mappeddatafieldcollection/) - A collection that represents mapped data fields for the mail merge operation.
### getMergeDuplicateRegions() {#getMergeDuplicateRegions}
```
public boolean getMergeDuplicateRegions()
```


Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to work with duplicate mail merge regions.

```

 public void mergeDuplicateRegions(boolean isMergeDuplicateRegions) throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMergeDuplicateRegions();
     DataTable dataTable = createSourceTableMergeDuplicateRegions();

     // If this property is false, the first region will be merged
     // while the MERGEFIELDs of the second one will be left in the pre-merge state
     // To get both regions merged we would have to execute the mail merge twice, on a table of the same name
     // If this is set to true, both regions will be affected by the merge
     doc.getMailMerge().setMergeDuplicateRegions(isMergeDuplicateRegions);

     doc.getMailMerge().executeWithRegions(dataTable);
     doc.save(getArtifactsDir() + "MailMerge.MergeDuplicateRegions.docx");
 }

 public static Object[][] mergeDuplicateRegionsDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Return a document that contains two duplicate mail merge regions (sharing the same name in the "TableStart/End" tags).
 /// 
 private static Document createSourceDocMergeDuplicateRegions() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" MERGEFIELD TableStart:MergeRegion");
     builder.insertField(" MERGEFIELD Column1");
     builder.insertField(" MERGEFIELD TableEnd:MergeRegion");
     builder.insertParagraph();

     builder.insertField(" MERGEFIELD TableStart:MergeRegion");
     builder.insertField(" MERGEFIELD Column2");
     builder.insertField(" MERGEFIELD TableEnd:MergeRegion");

     return doc;
 }

 /// 
 /// Create a data table with one row and two columns.
 /// 
 private static DataTable createSourceTableMergeDuplicateRegions() {
     DataTable dataTable = new DataTable("MergeRegion");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value 1", "Value 2");

     return dataTable;
 }
 
```

**Returns:**
boolean - A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.
### getMergeWholeDocument() {#getMergeWholeDocument}
```
public boolean getMergeWholeDocument()
```


Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows the relationship between mail merges with regions and field updating.

```

 public void mergeWholeDocument(boolean doMergeWholeDocument) throws Exception {
     // Create a document and data table that will both be merged
     Document doc = createSourceDocMergeWholeDocument();
     DataTable dataTable = createSourceTableMergeWholeDocument();

     // A regular mail merge will update all fields in the document as part of the procedure,
     // which will happen if this property is set to true
     // Otherwise, a mail merge with regions will only update fields
     // within a mail merge region which matches the name of the DataTable
     doc.getMailMerge().setMergeWholeDocument(doMergeWholeDocument);
     doc.getMailMerge().executeWithRegions(dataTable);

     // If true, all fields in the document will be updated upon merging
     // In this case that property is false, so the first QUOTE field will not be updated and will not show a value,
     // but the second one inside the region designated by the data table name will show the correct value
     doc.save(getArtifactsDir() + "MailMerge.MergeWholeDocument.docx");

     Assert.assertEquals(doMergeWholeDocument, doc.getText().contains("This QUOTE field is outside of the \"MyTable\" merge region."));
 }

 public static Object[][] mergeWholeDocumentDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// Create a document with a QUOTE field outside and one more inside a mail merge region called "MyTable"
 /// 
 private static Document createSourceDocMergeWholeDocument() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert QUOTE field outside of any mail merge regions
     FieldQuote field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
     field.setText("This QUOTE field is outside of the \"MyTable\" merge region.");

     // Start "MyTable" merge region
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD TableStart:MyTable");

     // Insert QUOTE field inside "MyTable" merge region
     field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
     field.setText("This QUOTE field is inside the \"MyTable\" merge region.");
     builder.insertParagraph();

     // Add a MERGEFIELD for a column in the data table, end the "MyTable" region and return the document
     builder.insertField(" MERGEFIELD MyColumn");
     builder.insertField(" MERGEFIELD TableEnd:MyTable");

     return doc;
 }

 /// 
 /// Create a simple data table that will be used in a mail merge.
 /// 
 private static DataTable createSourceTableMergeWholeDocument() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("MyColumn");
     dataTable.getRows().add("MyValue");

     return dataTable;
 }
 
```

**Returns:**
boolean - A value indicating whether fields in whole document are updated while executing of a mail merge with regions.
### getPreserveUnusedTags() {#getPreserveUnusedTags}
```
public boolean getPreserveUnusedTags()
```


Gets a value indicating whether the unused "mustache" tags should be preserved.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to preserve the appearance of alternative mail merge tags that go unused during a mail merge.

```

 public void preserveUnusedTags(boolean doPreserveUnusedTags) throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocWithAlternativeMergeFields();
     DataTable dataTable = createSourceTablePreserveUnusedTags();

     // By default, alternative merge tags that can't receive data because the data source has no columns with their name
     // are converted to and left on display as MERGEFIELDs after the mail merge
     // We can preserve their original appearance setting this attribute to true
     doc.getMailMerge().setPreserveUnusedTags(doPreserveUnusedTags);
     doc.getMailMerge().execute(dataTable);

     doc.save(getArtifactsDir() + "MailMerge.PreserveUnusedTags.docx");

     Assert.assertEquals(doc.getText().contains("{{ Column2 }}"), doPreserveUnusedTags);
 }

 public static Object[][] preserveUnusedTagsDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// Create a document and add two tags that can accept mail merge data that are not the traditional MERGEFIELDs.
 /// 
 private static Document createSourceDocWithAlternativeMergeFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("{{ Column1 }}");
     builder.writeln("{{ Column2 }}");

     // Our tags will only register as destinations for mail merge data if we set this to true
     doc.getMailMerge().setUseNonMergeFields(true);

     return doc;
 }

 /// 
 /// Create a simple data table with one column.
 /// 
 private static DataTable createSourceTablePreserveUnusedTags() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getRows().add("Value1");

     return dataTable;
 }
 
```

**Returns:**
boolean - A value indicating whether the unused "mustache" tags should be preserved.
### getRegionEndTag() {#getRegionEndTag}
```
public String getRegionEndTag()
```


Gets a mail merge region end tag.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Returns:**
java.lang.String - A mail merge region end tag.
### getRegionStartTag() {#getRegionStartTag}
```
public String getRegionStartTag()
```


Gets a mail merge region start tag.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Returns:**
java.lang.String - A mail merge region start tag.
### getRegionsByName(String regionName) {#getRegionsByName-java.lang.String}
```
public ArrayList getRegionsByName(String regionName)
```


Returns a collection of mail merge regions with the specified name.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| regionName | java.lang.String | Region name (case-insensitive). |

**Returns:**
java.util.ArrayList - The list of regions.
### getRegionsHierarchy() {#getRegionsHierarchy}
```
public MailMergeRegionInfo getRegionsHierarchy()
```


Returns a full hierarchy of regions (with fields) available in the document.

 **Remarks:** 

Hierarchy is returned in the form of the [MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo/) class.

 **Examples:** 

Shows how to get MailMergeRegionInfo and work with it.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo/) - Regions' hierarchy.
### getRestartListsAtEachSection() {#getRestartListsAtEachSection}
```
public boolean getRestartListsAtEachSection()
```


Gets a value indicating whether lists are restarted at each section after executing of a mail merge.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to control whether or not list numbering is restarted at each section when mail merge is performed.

```

 Document doc = new Document(getMyDir() + "Section breaks with numbering.docx");

 doc.getMailMerge().setRestartListsAtEachSection(false);
 doc.getMailMerge().execute(new String[0], new Object[0]);

 doc.save(getArtifactsDir() + "MailMerge.RestartListsAtEachSection.pdf");
 
```

**Returns:**
boolean - A value indicating whether lists are restarted at each section after executing of a mail merge.
### getRetainFirstSectionStart() {#getRetainFirstSectionStart}
```
public boolean getRetainFirstSectionStart()
```


Gets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.

 **Remarks:** 

The default value is  true .

**Returns:**
boolean - A value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.
### getTrimWhitespaces() {#getTrimWhitespaces}
```
public boolean getTrimWhitespaces()
```


Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to trimmed whitespaces from mail merge values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("MERGEFIELD myMergeField", null);

 doc.getMailMerge().setTrimWhitespaces(doTrimWhitespaces);
 doc.getMailMerge().execute(new String[]{"myMergeField"}, new Object[]{"\t hello world! "});

 if (doTrimWhitespaces)
     Assert.assertEquals("hello world!\f", doc.getText());
 else
     Assert.assertEquals("\t hello world! \f", doc.getText());
 
```

**Returns:**
boolean - A value indicating whether trailing and leading whitespaces are trimmed from mail merge values.
### getUnconditionalMergeFieldsAndRegions() {#getUnconditionalMergeFieldsAndRegions}
```
public boolean getUnconditionalMergeFieldsAndRegions()
```


Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to merge fields or regions regardless of the parent IF field's condition.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEFIELD nested inside an IF field
 // Since the statement of the IF field is false, the result of the inner MERGEFIELD will not be displayed
 // and the MERGEFIELD will not receive any data during a mail merge
 FieldIf fieldIf = (FieldIf) builder.insertField(" IF 1 = 2 ");
 builder.moveTo(fieldIf.getSeparator());
 builder.insertField(" MERGEFIELD  FullName ");

 // We can still count MERGEFIELDs inside false-statement IF fields if we set this flag to true
 doc.getMailMerge().setUnconditionalMergeFieldsAndRegions(doCountAllMergeFields);

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FullName");
 dataTable.getRows().add("James Bond");

 // Execute the mail merge
 doc.getMailMerge().execute(dataTable);

 // The result will not be visible in the document because the IF field is false, but the inner MERGEFIELD did indeed receive data
 doc.save(getArtifactsDir() + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

 if (doCountAllMergeFields)
     Assert.assertEquals("IF 1 = 2 \"James Bond\"", doc.getText().trim());
 else
     Assert.assertEquals("IF 1 = 2  MERGEFIELD  FullName «FullName»", doc.getText().trim());
 
```

**Returns:**
boolean - A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.
### getUseNonMergeFields() {#getUseNonMergeFields}
```
public boolean getUseNonMergeFields()
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

 **Remarks:** 

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

 **Examples:** 

Shows how to perform mail merge into merge fields and into additional fields types.

```

 doc.getMailMerge().setUseNonMergeFields(true);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getUseWholeParagraphAsRegion() {#getUseWholeParagraphAsRegion}
```
public boolean getUseWholeParagraphAsRegion()
```


Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows the relationship between mail merge regions and paragraphs.

```

 public void useWholeParagraphAsRegion() throws Exception {
     // Create a document with 2 mail merge regions in one paragraph and a table to which can fill one of the regions during a mail merge
     Document doc = createSourceDocWithNestedMergeRegions();
     DataTable dataTable = createSourceTableDataTableForOneRegion();

     // By default, a paragraph can belong to no more than one mail merge region
     // Our document breaks this rule so executing a mail merge with regions now will cause an exception to be thrown
     Assert.assertTrue(doc.getMailMerge().getUseWholeParagraphAsRegion());
     Assert.assertThrows(IllegalStateException.class, () -> doc.getMailMerge().executeWithRegions(dataTable));

     // If we set this variable to false, paragraphs and mail merge regions are independent so we can safely run our mail merge
     doc.getMailMerge().setUseWholeParagraphAsRegion(false);
     doc.getMailMerge().executeWithRegions(dataTable);

     // Our first region is populated, while our second is safely displayed as unused all across one paragraph
     doc.save(getArtifactsDir() + "MailMerge.UseWholeParagraphAsRegion.docx");
 }

 /// 
 /// Create a document with two mail merge regions sharing one paragraph.
 /// 
 private static Document createSourceDocWithNestedMergeRegions() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.write("Region 1: ");
     builder.insertField(" MERGEFIELD TableStart:MyTable");
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column2");
     builder.insertField(" MERGEFIELD TableEnd:MyTable");

     builder.write(", Region 2: ");
     builder.insertField(" MERGEFIELD TableStart:MyOtherTable");
     builder.insertField(" MERGEFIELD TableEnd:MyOtherTable");

     return doc;
 }

 /// 
 /// Create a data table that can populate one region during a mail merge.
 /// 
 private static DataTable createSourceTableDataTableForOneRegion() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value 1", "Value 2");

     return dataTable;
 }
 
```

**Returns:**
boolean - A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.
### setCleanupOptions(int value) {#setCleanupOptions-int}
```
public void setCleanupOptions(int value)
```


Sets a set of flags that specify what items should be removed during mail merge.

 **Examples:** 

Shows how to automatically remove unmerged merge fields during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Shows how to make sure empty paragraphs that result from merging fields with no data are removed from the document.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Shows how to instruct the mail merge engine to remove any containing fields from around a merge field during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A set of flags that specify what items should be removed during mail merge. The value must be a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants. |

### setCleanupParagraphsWithPunctuationMarks(boolean value) {#setCleanupParagraphsWithPunctuationMarks-boolean}
```
public void setCleanupParagraphsWithPunctuationMarks(boolean value)
```


Sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.

 **Remarks:** 

The default value is  true .

Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

 **Examples:** 

Shows how to remove paragraphs with punctuation marks after mail merge operation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.insertField("MERGEFIELD", "Option_1");
 mergeFieldOption1.setFieldName("Option_1");

 // Here is the complete list of cleanable punctuation marks:
 // !
 // ,
 // .
 // :
 // ;
 // ?
 // ¡
 // ¿
 builder.write(punctuationMark);

 FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.insertField("MERGEFIELD", "Option_2");
 mergeFieldOption2.setFieldName("Option_2");

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 // The default value of the option is true which means that the behavior was changed to mimic MS Word
 // If you rely on the old behavior are able to revert it by setting the option to false
 doc.getMailMerge().setCleanupParagraphsWithPunctuationMarks(isCleanupParagraphsWithPunctuationMarks);

 doc.getMailMerge().execute(new String[]{"Option_1", "Option_2"}, new Object[]{null, null});

 doc.save(getArtifactsDir() + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |

### setFieldMergingCallback(IFieldMergingCallback value) {#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback}
```
public void setFieldMergingCallback(IFieldMergingCallback value)
```


Occurs during mail merge when a mail merge field is encountered in the document.

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

Shows how to insert images stored in a database BLOB field into a report.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) | The corresponding [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) value. |

### setMailMergeCallback(IMailMergeCallback value) {#setMailMergeCallback-com.aspose.words.IMailMergeCallback}
```
public void setMailMergeCallback(IMailMergeCallback value)
```


Allows to handle particular events during mail merge.

 **Examples:** 

Shows how to define custom logic for handling events during mail merge.

```

 public void testTagsReplacedEventShouldRisedWithUseNonMergeFieldsOption() throws Exception {
     Document document = new Document();
     document.getMailMerge().setUseNonMergeFields(true);

     MailMergeCallbackStub mailMergeCallbackStub = new MailMergeCallbackStub();
     document.getMailMerge().setMailMergeCallback(mailMergeCallbackStub);

     document.getMailMerge().execute(new String[0], new Object[0]);

     Assert.assertEquals(mailMergeCallbackStub.getTagsReplacedCounter(), 1);
 }

 private static class MailMergeCallbackStub implements IMailMergeCallback {
     public void tagsReplaced() {
         mTagsReplacedCounter++;
     }

     public int getTagsReplacedCounter() {
         return mTagsReplacedCounter;
     }

     private int mTagsReplacedCounter;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) | The corresponding [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) value. |

### setMergeDuplicateRegions(boolean value) {#setMergeDuplicateRegions-boolean}
```
public void setMergeDuplicateRegions(boolean value)
```


Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to work with duplicate mail merge regions.

```

 public void mergeDuplicateRegions(boolean isMergeDuplicateRegions) throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocMergeDuplicateRegions();
     DataTable dataTable = createSourceTableMergeDuplicateRegions();

     // If this property is false, the first region will be merged
     // while the MERGEFIELDs of the second one will be left in the pre-merge state
     // To get both regions merged we would have to execute the mail merge twice, on a table of the same name
     // If this is set to true, both regions will be affected by the merge
     doc.getMailMerge().setMergeDuplicateRegions(isMergeDuplicateRegions);

     doc.getMailMerge().executeWithRegions(dataTable);
     doc.save(getArtifactsDir() + "MailMerge.MergeDuplicateRegions.docx");
 }

 public static Object[][] mergeDuplicateRegionsDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Return a document that contains two duplicate mail merge regions (sharing the same name in the "TableStart/End" tags).
 /// 
 private static Document createSourceDocMergeDuplicateRegions() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" MERGEFIELD TableStart:MergeRegion");
     builder.insertField(" MERGEFIELD Column1");
     builder.insertField(" MERGEFIELD TableEnd:MergeRegion");
     builder.insertParagraph();

     builder.insertField(" MERGEFIELD TableStart:MergeRegion");
     builder.insertField(" MERGEFIELD Column2");
     builder.insertField(" MERGEFIELD TableEnd:MergeRegion");

     return doc;
 }

 /// 
 /// Create a data table with one row and two columns.
 /// 
 private static DataTable createSourceTableMergeDuplicateRegions() {
     DataTable dataTable = new DataTable("MergeRegion");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value 1", "Value 2");

     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |

### setMergeWholeDocument(boolean value) {#setMergeWholeDocument-boolean}
```
public void setMergeWholeDocument(boolean value)
```


Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows the relationship between mail merges with regions and field updating.

```

 public void mergeWholeDocument(boolean doMergeWholeDocument) throws Exception {
     // Create a document and data table that will both be merged
     Document doc = createSourceDocMergeWholeDocument();
     DataTable dataTable = createSourceTableMergeWholeDocument();

     // A regular mail merge will update all fields in the document as part of the procedure,
     // which will happen if this property is set to true
     // Otherwise, a mail merge with regions will only update fields
     // within a mail merge region which matches the name of the DataTable
     doc.getMailMerge().setMergeWholeDocument(doMergeWholeDocument);
     doc.getMailMerge().executeWithRegions(dataTable);

     // If true, all fields in the document will be updated upon merging
     // In this case that property is false, so the first QUOTE field will not be updated and will not show a value,
     // but the second one inside the region designated by the data table name will show the correct value
     doc.save(getArtifactsDir() + "MailMerge.MergeWholeDocument.docx");

     Assert.assertEquals(doMergeWholeDocument, doc.getText().contains("This QUOTE field is outside of the \"MyTable\" merge region."));
 }

 public static Object[][] mergeWholeDocumentDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// Create a document with a QUOTE field outside and one more inside a mail merge region called "MyTable"
 /// 
 private static Document createSourceDocMergeWholeDocument() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert QUOTE field outside of any mail merge regions
     FieldQuote field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
     field.setText("This QUOTE field is outside of the \"MyTable\" merge region.");

     // Start "MyTable" merge region
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD TableStart:MyTable");

     // Insert QUOTE field inside "MyTable" merge region
     field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
     field.setText("This QUOTE field is inside the \"MyTable\" merge region.");
     builder.insertParagraph();

     // Add a MERGEFIELD for a column in the data table, end the "MyTable" region and return the document
     builder.insertField(" MERGEFIELD MyColumn");
     builder.insertField(" MERGEFIELD TableEnd:MyTable");

     return doc;
 }

 /// 
 /// Create a simple data table that will be used in a mail merge.
 /// 
 private static DataTable createSourceTableMergeWholeDocument() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("MyColumn");
     dataTable.getRows().add("MyValue");

     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether fields in whole document are updated while executing of a mail merge with regions. |

### setPreserveUnusedTags(boolean value) {#setPreserveUnusedTags-boolean}
```
public void setPreserveUnusedTags(boolean value)
```


Sets a value indicating whether the unused "mustache" tags should be preserved.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to preserve the appearance of alternative mail merge tags that go unused during a mail merge.

```

 public void preserveUnusedTags(boolean doPreserveUnusedTags) throws Exception {
     // Create a document and table that we will merge
     Document doc = createSourceDocWithAlternativeMergeFields();
     DataTable dataTable = createSourceTablePreserveUnusedTags();

     // By default, alternative merge tags that can't receive data because the data source has no columns with their name
     // are converted to and left on display as MERGEFIELDs after the mail merge
     // We can preserve their original appearance setting this attribute to true
     doc.getMailMerge().setPreserveUnusedTags(doPreserveUnusedTags);
     doc.getMailMerge().execute(dataTable);

     doc.save(getArtifactsDir() + "MailMerge.PreserveUnusedTags.docx");

     Assert.assertEquals(doc.getText().contains("{{ Column2 }}"), doPreserveUnusedTags);
 }

 public static Object[][] preserveUnusedTagsDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// Create a document and add two tags that can accept mail merge data that are not the traditional MERGEFIELDs.
 /// 
 private static Document createSourceDocWithAlternativeMergeFields() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("{{ Column1 }}");
     builder.writeln("{{ Column2 }}");

     // Our tags will only register as destinations for mail merge data if we set this to true
     doc.getMailMerge().setUseNonMergeFields(true);

     return doc;
 }

 /// 
 /// Create a simple data table with one column.
 /// 
 private static DataTable createSourceTablePreserveUnusedTags() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getRows().add("Value1");

     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the unused "mustache" tags should be preserved. |

### setRegionEndTag(String value) {#setRegionEndTag-java.lang.String}
```
public void setRegionEndTag(String value)
```


Sets a mail merge region end tag.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region end tag. |

### setRegionStartTag(String value) {#setRegionStartTag-java.lang.String}
```
public void setRegionStartTag(String value)
```


Sets a mail merge region start tag.

 **Examples:** 

Shows how to create, list, and read mail merge regions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region start tag. |

### setRestartListsAtEachSection(boolean value) {#setRestartListsAtEachSection-boolean}
```
public void setRestartListsAtEachSection(boolean value)
```


Sets a value indicating whether lists are restarted at each section after executing of a mail merge.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to control whether or not list numbering is restarted at each section when mail merge is performed.

```

 Document doc = new Document(getMyDir() + "Section breaks with numbering.docx");

 doc.getMailMerge().setRestartListsAtEachSection(false);
 doc.getMailMerge().execute(new String[0], new Object[0]);

 doc.save(getArtifactsDir() + "MailMerge.RestartListsAtEachSection.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether lists are restarted at each section after executing of a mail merge. |

### setRetainFirstSectionStart(boolean value) {#setRetainFirstSectionStart-boolean}
```
public void setRetainFirstSectionStart(boolean value)
```


Sets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.

 **Remarks:** 

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |

### setTrimWhitespaces(boolean value) {#setTrimWhitespaces-boolean}
```
public void setTrimWhitespaces(boolean value)
```


Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to trimmed whitespaces from mail merge values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("MERGEFIELD myMergeField", null);

 doc.getMailMerge().setTrimWhitespaces(doTrimWhitespaces);
 doc.getMailMerge().execute(new String[]{"myMergeField"}, new Object[]{"\t hello world! "});

 if (doTrimWhitespaces)
     Assert.assertEquals("hello world!\f", doc.getText());
 else
     Assert.assertEquals("\t hello world! \f", doc.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |

### setUnconditionalMergeFieldsAndRegions(boolean value) {#setUnconditionalMergeFieldsAndRegions-boolean}
```
public void setUnconditionalMergeFieldsAndRegions(boolean value)
```


Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to merge fields or regions regardless of the parent IF field's condition.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEFIELD nested inside an IF field
 // Since the statement of the IF field is false, the result of the inner MERGEFIELD will not be displayed
 // and the MERGEFIELD will not receive any data during a mail merge
 FieldIf fieldIf = (FieldIf) builder.insertField(" IF 1 = 2 ");
 builder.moveTo(fieldIf.getSeparator());
 builder.insertField(" MERGEFIELD  FullName ");

 // We can still count MERGEFIELDs inside false-statement IF fields if we set this flag to true
 doc.getMailMerge().setUnconditionalMergeFieldsAndRegions(doCountAllMergeFields);

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FullName");
 dataTable.getRows().add("James Bond");

 // Execute the mail merge
 doc.getMailMerge().execute(dataTable);

 // The result will not be visible in the document because the IF field is false, but the inner MERGEFIELD did indeed receive data
 doc.save(getArtifactsDir() + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

 if (doCountAllMergeFields)
     Assert.assertEquals("IF 1 = 2 \"James Bond\"", doc.getText().trim());
 else
     Assert.assertEquals("IF 1 = 2  MERGEFIELD  FullName «FullName»", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |

### setUseNonMergeFields(boolean value) {#setUseNonMergeFields-boolean}
```
public void setUseNonMergeFields(boolean value)
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

 **Remarks:** 

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

 **Examples:** 

Shows how to perform mail merge into merge fields and into additional fields types.

```

 doc.getMailMerge().setUseNonMergeFields(true);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseWholeParagraphAsRegion(boolean value) {#setUseWholeParagraphAsRegion-boolean}
```
public void setUseWholeParagraphAsRegion(boolean value)
```


Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows the relationship between mail merge regions and paragraphs.

```

 public void useWholeParagraphAsRegion() throws Exception {
     // Create a document with 2 mail merge regions in one paragraph and a table to which can fill one of the regions during a mail merge
     Document doc = createSourceDocWithNestedMergeRegions();
     DataTable dataTable = createSourceTableDataTableForOneRegion();

     // By default, a paragraph can belong to no more than one mail merge region
     // Our document breaks this rule so executing a mail merge with regions now will cause an exception to be thrown
     Assert.assertTrue(doc.getMailMerge().getUseWholeParagraphAsRegion());
     Assert.assertThrows(IllegalStateException.class, () -> doc.getMailMerge().executeWithRegions(dataTable));

     // If we set this variable to false, paragraphs and mail merge regions are independent so we can safely run our mail merge
     doc.getMailMerge().setUseWholeParagraphAsRegion(false);
     doc.getMailMerge().executeWithRegions(dataTable);

     // Our first region is populated, while our second is safely displayed as unused all across one paragraph
     doc.save(getArtifactsDir() + "MailMerge.UseWholeParagraphAsRegion.docx");
 }

 /// 
 /// Create a document with two mail merge regions sharing one paragraph.
 /// 
 private static Document createSourceDocWithNestedMergeRegions() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.write("Region 1: ");
     builder.insertField(" MERGEFIELD TableStart:MyTable");
     builder.insertField(" MERGEFIELD Column1");
     builder.write(", ");
     builder.insertField(" MERGEFIELD Column2");
     builder.insertField(" MERGEFIELD TableEnd:MyTable");

     builder.write(", Region 2: ");
     builder.insertField(" MERGEFIELD TableStart:MyOtherTable");
     builder.insertField(" MERGEFIELD TableEnd:MyOtherTable");

     return doc;
 }

 /// 
 /// Create a data table that can populate one region during a mail merge.
 /// 
 private static DataTable createSourceTableDataTableForOneRegion() {
     DataTable dataTable = new DataTable("MyTable");
     dataTable.getColumns().add("Column1");
     dataTable.getColumns().add("Column2");
     dataTable.getRows().add("Value 1", "Value 2");

     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

