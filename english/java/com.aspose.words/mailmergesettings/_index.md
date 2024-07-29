---
title: MailMergeSettings
linktitle: MailMergeSettings
second_title: Aspose.Words for Java
description: Specifies all of the mail merge information for a document in Java.
type: docs
weight: 417
url: /java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Specifies all of the mail merge information for a document.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

You do not normally need to create objects of this class directly because Mail merge settings of a document are always available via the [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) property.

To detect whether this document is a mail merge main document, check the value of the [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) property.

To remove mail merge settings and data source information from a document you can use the [clear()](../../com.aspose.words/mailmergesettings/\#clear) method. Aspose.Words will not write mail merge settings to a document if the [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) property is set to [MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) or the [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) property is set to [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

The best way to learn how to use the properties of this object is to create a document with a desired data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties of the [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) and [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) objects. This is a good approach to take if you want to learn how to programmatically configure a data source, for example.

Aspose.Words preserves mail merge information when loading, saving and converting documents between different formats, but does not use this information when performing its own mail merge using the [MailMerge](../../com.aspose.words/mailmerge/) object.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Clears the mail merge settings in such a way that when the document is saved, no mail merge settings will be saved and it will become a normal document. |
| [deepClone()](#deepClone) | Returns a deep clone of this object. |
| [getActiveRecord()](#getActiveRecord) | Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | Specifies the column within the data source that contains e-mail addresses. |
| [getCheckErrors()](#getCheckErrors) | Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge. |
| [getConnectString()](#getConnectString) | Specifies the connection string used to connect to an external data source. |
| [getDataSource()](#getDataSource) | Specifies the path to the mail-merge data source. |
| [getDataType()](#getDataType) | Specifies the type of the mail-merge data source and the method of data access. |
| [getDestination()](#getDestination) | Specifies how Microsoft Word will output the results of a mail merge. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. |
| [getHeaderSource()](#getHeaderSource) | Specifies the path to the mail-merge header source. |
| [getLinkToQuery()](#getLinkToQuery) | Not sure about this one. |
| [getMailAsAttachment()](#getMailAsAttachment) | Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather than the body of the actual e-mail. |
| [getMailSubject()](#getMailSubject) | Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. |
| [getMainDocumentType()](#getMainDocumentType) | Specifies the mail-merge main document type. |
| [getOdso()](#getOdso) | Gets the object that specifies the Office Data Source Object (ODSO) settings. |
| [getQuery()](#getQuery) | Contains the Structured Query Language string that shall be run against the specified external data source to return the set of records which shall be imported into the document when the mail merge operation is performed. |
| [getViewMergedData()](#getViewMergedData) | Specifies that Microsoft Word shall display the data from the specified external data source where merge fields have been inserted (e.g. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Specifies the column within the data source that contains e-mail addresses. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Specifies the connection string used to connect to an external data source. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Specifies the path to the mail-merge data source. |
| [setDataType(int value)](#setDataType-int) | Specifies the type of the mail-merge data source and the method of data access. |
| [setDestination(int value)](#setDestination-int) | Specifies how Microsoft Word will output the results of a mail merge. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Specifies the path to the mail-merge header source. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Not sure about this one. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather than the body of the actual e-mail. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Specifies the mail-merge main document type. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Sets the object that specifies the Office Data Source Object (ODSO) settings. |
| [setQuery(String value)](#setQuery-java.lang.String) | Contains the Structured Query Language string that shall be run against the specified external data source to return the set of records which shall be imported into the document when the mail merge operation is performed. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Specifies that Microsoft Word shall display the data from the specified external data source where merge fields have been inserted (e.g. |
### clear() {#clear}
```
public void clear()
```


Clears the mail merge settings in such a way that when the document is saved, no mail merge settings will be saved and it will become a normal document.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Returns a deep clone of this object.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1.

**Returns:**
int - The corresponding  int  value.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Specifies the column within the data source that contains e-mail addresses. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge. The default value is [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/) constants.
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Specifies the connection string used to connect to an external data source. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Specifies the path to the mail-merge data source. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDataType() {#getDataType}
```
public int getDataType()
```


Specifies the type of the mail-merge data source and the method of data access. The default value is [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [MailMergeDataType](../../com.aspose.words/mailmergedatatype/) constants.
### getDestination() {#getDestination}
```
public int getDestination()
```


Specifies how Microsoft Word will output the results of a mail merge. The default value is [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [MailMergeDestination](../../com.aspose.words/mailmergedestination/) constants.
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Specifies the path to the mail-merge header source. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Not sure about this one. The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference to an external query file which contains the actual query. The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather than the body of the actual e-mail. The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Specifies the mail-merge main document type. The default value is [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

The main document is the document that contains information that is the same for each version of the merged document.

**Returns:**
int - The corresponding  int  value. The returned value is one of [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/) constants.
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Gets the object that specifies the Office Data Source Object (ODSO) settings.

 **Remarks:** 

This object is never  null .

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Contains the Structured Query Language string that shall be run against the specified external data source to return the set of records which shall be imported into the document when the mail merge operation is performed. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Specifies that Microsoft Word shall display the data from the specified external data source where merge fields have been inserted (e.g. preview merged data). The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Specifies the column within the data source that contains e-mail addresses. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge. The default value is [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/) constants. |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Specifies the connection string used to connect to an external data source. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Specifies the path to the mail-merge data source. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Specifies the type of the mail-merge data source and the method of data access. The default value is [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MailMergeDataType](../../com.aspose.words/mailmergedatatype/) constants. |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Specifies how Microsoft Word will output the results of a mail merge. The default value is [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MailMergeDestination](../../com.aspose.words/mailmergedestination/) constants. |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Specifies the path to the mail-merge header source. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Not sure about this one. The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference to an external query file which contains the actual query. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather than the body of the actual e-mail. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Specifies the mail-merge main document type. The default value is [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

The main document is the document that contains information that is the same for each version of the merged document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/) constants. |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Sets the object that specifies the Office Data Source Object (ODSO) settings.

 **Remarks:** 

This object is never  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | The object that specifies the Office Data Source Object (ODSO) settings. |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Contains the Structured Query Language string that shall be run against the specified external data source to return the set of records which shall be imported into the document when the mail merge operation is performed. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Specifies that Microsoft Word shall display the data from the specified external data source where merge fields have been inserted (e.g. preview merged data). The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

