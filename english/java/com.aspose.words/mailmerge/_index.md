---
title: MailMerge
linktitle: MailMerge
second_title: Aspose.Words for Java API Reference
description: Represents the mail merge functionality in Java.
type: docs
weight: 382
url: /java/com.aspose.words/mailmerge/
---

**Inheritance:**
java.lang.Object
```
public class MailMerge
```

Represents the mail merge functionality.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

For mail merge operation to work, the document should contain Word MERGEFIELD and optionally NEXT fields. During mail merge operation, merge fields in the document are replaced with values from your data source.

There are two distinct ways to use mail merge: with mail merge regions and without.

The simplest mail merge is without regions and it is very similar to how mail merge works in Word. Use  Execute  methods to merge information from some data source such as **DataTable**, **DataSet** or an array of objects into your document. The [MailMerge](../../com.aspose.words/mailmerge/) object processes all records of the data source and copies and appends content of the whole document for each record.

Note that when [MailMerge](../../com.aspose.words/mailmerge/) object encounters a NEXT field, it selects next record in the data source and continues merging without copying any content.

Use [executeWithRegions(com.aspose.words.IMailMergeDataSource)](../../com.aspose.words/mailmerge/\#executeWithRegions-com.aspose.words.IMailMergeDataSource) and other overloads to merge information into a document with mail merge regions defined. You can use  or  as data sources for this operation.

You need to use mail merge regions if you want to dynamically grow portions inside the document. Without mail merge regions whole document will be repeated for every record of the data source.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [deleteFields()](#deleteFields) | Removes mail merge related fields from the document. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
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
| [getClass()](#getClass) |  |
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
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
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
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### deleteFields() {#deleteFields}
```
public void deleteFields()
```


Removes mail merge related fields from the document.

This method removes MERGEFIELD and NEXT fields from the document.

This method could be useful if your mail merge operation does not always need to populate all fields in the document. Use this method to remove all remaining mail merge fields.

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### execute(IMailMergeDataSource dataSource) {#execute-com.aspose.words.IMailMergeDataSource}
```
public void execute(IMailMergeDataSource dataSource)
```


Performs a mail merge from a custom data source.

Use this method to fill mail merge fields in the document with values from any data source such as a list or hashtable or objects. You need to write your own class that implements the [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) interface.

You can use this method only when [FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate-boolean) is  false , that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### execute(System.Data.DataRow row) {#execute-com.aspose.words.net.System.Data.DataRow}
```
public void execute(System.Data.DataRow row)
```


Performs mail merge from a **DataRow** into the document.

Use this method to fill mail merge fields in the document with values from a **DataRow**.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(System.Data.DataTable table) {#execute-com.aspose.words.net.System.Data.DataTable}
```
public void execute(System.Data.DataTable table)
```


Performs mail merge from a com.aspose.words.net.System.Data.DataTable into the document.

Use this method to fill mail merge fields in the document with values from a **DataTable**.

All records from the table are merged into the document.

You can use NEXT field in the Word document to cause [MailMerge](../../com.aspose.words/mailmerge/) object to select next record from the **DataTable** and continue merging. This can be used when creating documents such as mailing labels.

When [MailMerge](../../com.aspose.words/mailmerge/) object reaches end of the main document and there are still more rows in the **DataTable**, it copies entire content of the main document and appends it to the end of the destination document using a section break as a separator.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(System.Data.DataView dataView) {#execute-com.aspose.words.net.System.Data.DataView}
```
public void execute(System.Data.DataView dataView)
```


Performs mail merge from a **DataView** into the document.

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

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) | Data source for the mail merge operation. |

### execute(String[] fieldNames, Object[] values) {#execute-java.lang.String---java.lang.Object}
```
public void execute(String[] fieldNames, Object[] values)
```


Performs a mail merge operation.  Performs a mail merge operation for a single record.

Use this method to fill mail merge fields in the document with values from an array of objects.

This method merges data for one record only. The array of field names and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the [MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) option.

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

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own classes that implement the [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot/) and [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) interfaces.

You can use this method only when [FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions/\#isBidiTextSupportedOnUpdate-boolean) is  false , that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceRoot | [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot/) | An object that implements the custom mail merge data source root interface. |

### executeWithRegions(System.Data.DataSet dataSet) {#executeWithRegions-com.aspose.words.net.System.Data.DataSet}
```
public void executeWithRegions(System.Data.DataSet dataSet)
```


Performs a mail merge operation into a document with mail merge regions. Supports parent-child (master-detail) data sources and nested mail merge regions.  Performs mail merge from a **DataSet** into a document with mail merge regions.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | **DataSet** that contains data to be inserted into mail merge fields. |

### executeWithRegions(System.Data.DataTable dataTable) {#executeWithRegions-com.aspose.words.net.System.Data.DataTable}
```
public void executeWithRegions(System.Data.DataTable dataTable)
```


Performs mail merge from a **DataTable** into the document with mail merge regions.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Data source for the mail merge operation. The table must have its [DataTable.getTableName()](../../com.aspose.words.net.system.data/datatable/\#getTableName) / [DataTable.setTableName(java.lang.String)](../../com.aspose.words.net.system.data/datatable/\#setTableName-java.lang.String) property set. |

### executeWithRegions(System.Data.DataView dataView) {#executeWithRegions-com.aspose.words.net.System.Data.DataView}
```
public void executeWithRegions(System.Data.DataView dataView)
```


Performs mail merge from a **DataView** into the document with mail merge regions.

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

The document must have a mail merge region defined with name that matches **DataView.Table.TableName**.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview/) | Data source for the mail merge operation. The source table of the **DataView** must have its **TableName** property set. |

### executeWithRegions(System.Data.IDataReader dataReader, String tableName) {#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String}
```
public void executeWithRegions(System.Data.IDataReader dataReader, String tableName)
```


Performs mail merge from **IDataReader** into the document with mail merge regions.

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) | Source of the data records for mail merge such as **OleDbDataReader** or **SqlDataReader**. |
| tableName | java.lang.String | Name of the mail merge region in the document to populate. |

### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCleanupOptions() {#getCleanupOptions}
```
public int getCleanupOptions()
```


Gets a set of flags that specify what items should be removed during mail merge.

**Returns:**
int - A set of flags that specify what items should be removed during mail merge. The returned value is a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants.
### getCleanupParagraphsWithPunctuationMarks() {#getCleanupParagraphsWithPunctuationMarks}
```
public boolean getCleanupParagraphsWithPunctuationMarks()
```


Gets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. The default value is  true . Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

**Returns:**
boolean - A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.
### getFieldMergingCallback() {#getFieldMergingCallback}
```
public IFieldMergingCallback getFieldMergingCallback()
```


Occurs during mail merge when a mail merge field is encountered in the document.

**Returns:**
[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) - The corresponding [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) value.
### getFieldNames() {#getFieldNames}
```
public String[] getFieldNames()
```


Returns a collection of mail merge field names available in the document.

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

A new string array is created on every call.

Includes "mustache" field names if [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is  true .

**Returns:**
java.lang.String[]
### getFieldNamesForRegion(String regionName) {#getFieldNamesForRegion-java.lang.String}
```
public String[] getFieldNamesForRegion(String regionName)
```


Get mail merge field names from the region.  Returns a collection of mail merge field names available in the region.

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the very first region is processed.

A new string array is created on every call.

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

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the Nth region (zero-based) is processed.

A new string array is created on every call.

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

**Returns:**
[IMailMergeCallback](../../com.aspose.words/imailmergecallback/) - The corresponding [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) value.
### getMappedDataFields() {#getMappedDataFields}
```
public MappedDataFieldCollection getMappedDataFields()
```


Returns a collection that represents mapped data fields for the mail merge operation.

Mapped data fields allow to automatically map between names of fields in your data source and names of mail merge fields in the document.

**Returns:**
[MappedDataFieldCollection](../../com.aspose.words/mappeddatafieldcollection/) - A collection that represents mapped data fields for the mail merge operation.
### getMergeDuplicateRegions() {#getMergeDuplicateRegions}
```
public boolean getMergeDuplicateRegions()
```


Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. The default value is  false .

**Returns:**
boolean - A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.
### getMergeWholeDocument() {#getMergeWholeDocument}
```
public boolean getMergeWholeDocument()
```


Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. The default value is  false .

**Returns:**
boolean - A value indicating whether fields in whole document are updated while executing of a mail merge with regions.
### getPreserveUnusedTags() {#getPreserveUnusedTags}
```
public boolean getPreserveUnusedTags()
```


Gets a value indicating whether the unused "mustache" tags should be preserved. The default value is  false .

**Returns:**
boolean - A value indicating whether the unused "mustache" tags should be preserved.
### getRegionEndTag() {#getRegionEndTag}
```
public String getRegionEndTag()
```


Gets a mail merge region end tag.

**Returns:**
java.lang.String - A mail merge region end tag.
### getRegionStartTag() {#getRegionStartTag}
```
public String getRegionStartTag()
```


Gets a mail merge region start tag.

**Returns:**
java.lang.String - A mail merge region start tag.
### getRegionsByName(String regionName) {#getRegionsByName-java.lang.String}
```
public ArrayList getRegionsByName(String regionName)
```


Returns a collection of mail merge regions with the specified name.

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

Hierarchy is returned in the form of the [MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo/) class.

**Returns:**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo/) - Regions' hierarchy.
### getRestartListsAtEachSection() {#getRestartListsAtEachSection}
```
public boolean getRestartListsAtEachSection()
```


Gets a value indicating whether lists are restarted at each section after executing of a mail merge. The default value is  true .

**Returns:**
boolean - A value indicating whether lists are restarted at each section after executing of a mail merge.
### getRetainFirstSectionStart() {#getRetainFirstSectionStart}
```
public boolean getRetainFirstSectionStart()
```


Gets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. The default value is  true .

**Returns:**
boolean - A value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.
### getTrimWhitespaces() {#getTrimWhitespaces}
```
public boolean getTrimWhitespaces()
```


Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. The default value is  true .

**Returns:**
boolean - A value indicating whether trailing and leading whitespaces are trimmed from mail merge values.
### getUnconditionalMergeFieldsAndRegions() {#getUnconditionalMergeFieldsAndRegions}
```
public boolean getUnconditionalMergeFieldsAndRegions()
```


Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. The default value is  false .

**Returns:**
boolean - A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.
### getUseNonMergeFields() {#getUseNonMergeFields}
```
public boolean getUseNonMergeFields()
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

**Returns:**
boolean - The corresponding  boolean  value.
### getUseWholeParagraphAsRegion() {#getUseWholeParagraphAsRegion}
```
public boolean getUseWholeParagraphAsRegion()
```


Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. The default value is  true .

**Returns:**
boolean - A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setCleanupOptions(int value) {#setCleanupOptions-int}
```
public void setCleanupOptions(int value)
```


Sets a set of flags that specify what items should be removed during mail merge.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A set of flags that specify what items should be removed during mail merge. The value must be a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants. |

### setCleanupParagraphsWithPunctuationMarks(boolean value) {#setCleanupParagraphsWithPunctuationMarks-boolean}
```
public void setCleanupParagraphsWithPunctuationMarks(boolean value)
```


Sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. The default value is  true . Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |

### setFieldMergingCallback(IFieldMergingCallback value) {#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback}
```
public void setFieldMergingCallback(IFieldMergingCallback value)
```


Occurs during mail merge when a mail merge field is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) | The corresponding [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback/) value. |

### setMailMergeCallback(IMailMergeCallback value) {#setMailMergeCallback-com.aspose.words.IMailMergeCallback}
```
public void setMailMergeCallback(IMailMergeCallback value)
```


Allows to handle particular events during mail merge.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) | The corresponding [IMailMergeCallback](../../com.aspose.words/imailmergecallback/) value. |

### setMergeDuplicateRegions(boolean value) {#setMergeDuplicateRegions-boolean}
```
public void setMergeDuplicateRegions(boolean value)
```


Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |

### setMergeWholeDocument(boolean value) {#setMergeWholeDocument-boolean}
```
public void setMergeWholeDocument(boolean value)
```


Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether fields in whole document are updated while executing of a mail merge with regions. |

### setPreserveUnusedTags(boolean value) {#setPreserveUnusedTags-boolean}
```
public void setPreserveUnusedTags(boolean value)
```


Sets a value indicating whether the unused "mustache" tags should be preserved. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the unused "mustache" tags should be preserved. |

### setRegionEndTag(String value) {#setRegionEndTag-java.lang.String}
```
public void setRegionEndTag(String value)
```


Sets a mail merge region end tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region end tag. |

### setRegionStartTag(String value) {#setRegionStartTag-java.lang.String}
```
public void setRegionStartTag(String value)
```


Sets a mail merge region start tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region start tag. |

### setRestartListsAtEachSection(boolean value) {#setRestartListsAtEachSection-boolean}
```
public void setRestartListsAtEachSection(boolean value)
```


Sets a value indicating whether lists are restarted at each section after executing of a mail merge. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether lists are restarted at each section after executing of a mail merge. |

### setRetainFirstSectionStart(boolean value) {#setRetainFirstSectionStart-boolean}
```
public void setRetainFirstSectionStart(boolean value)
```


Sets a value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the [PageSetup.getSectionStart()](../../com.aspose.words/pagesetup/\#getSectionStart) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup/\#setSectionStart-int) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |

### setTrimWhitespaces(boolean value) {#setTrimWhitespaces-boolean}
```
public void setTrimWhitespaces(boolean value)
```


Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |

### setUnconditionalMergeFieldsAndRegions(boolean value) {#setUnconditionalMergeFieldsAndRegions-boolean}
```
public void setUnconditionalMergeFieldsAndRegions(boolean value)
```


Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |

### setUseNonMergeFields(boolean value) {#setUseNonMergeFields-boolean}
```
public void setUseNonMergeFields(boolean value)
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmerge/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseWholeParagraphAsRegion(boolean value) {#setUseWholeParagraphAsRegion-boolean}
```
public void setUseWholeParagraphAsRegion(boolean value)
```


Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

