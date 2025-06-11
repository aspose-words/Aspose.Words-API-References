---
title: Odso
linktitle: Odso
second_title: Aspose.Words for Java
description: Specifies the Office Data Source Object ODSO settings for a mail merge data source in Java.
type: docs
weight: 481
url: /java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

ODSO seems to be the "new" way the newer Microsoft Word versions prefer to use when specifying certain types of data sources for a mail merge document. ODSO probably first appeared in Microsoft Word 2000.

The use of ODSO is poorly documented and the best way to learn how to use the properties of this object is to create a document with a desired data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties of the [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) and [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) objects. This is a good approach to take if you want to learn how to programmatically configure a data source, for example.

You do not normally need to create objects of this class directly because ODSO settings are always available via the [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) property.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Returns a deep clone of this object. |
| [getColumnDelimiter()](#getColumnDelimiter) | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. |
| [getDataSource()](#getDataSource) | Specifies the location of the external data source to be connected to a document to perform the mail merge. |
| [getDataSourceType()](#getDataSourceType) | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. |
| [getFieldMapDatas()](#getFieldMapDatas) | Gets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. |
| [getRecipientDatas()](#getRecipientDatas) | Gets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. |
| [getTableName()](#getTableName) | Specifies the particular set of data that a source shall be connected to within an external data source. |
| [getUdlConnectString()](#getUdlConnectString) | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Specifies the location of the external data source to be connected to a document to perform the mail merge. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Sets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. |
| [setTableName(String value)](#setTableName-java.lang.String) | Specifies the particular set of data that a source shall be connected to within an external data source. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Returns a deep clone of this object.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined.

 **Remarks:** 

RK I have never seen this in use.

**Returns:**
char - The corresponding  char  value.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

This setting is purely a suggestion of the data source type that is being used for this mail merge.

**Returns:**
int - The corresponding  int  value. The returned value is one of [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/) constants.
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Gets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. This object is never  null .

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is  false .

 **Remarks:** 

RK I have never seen this in use.

**Returns:**
boolean - The corresponding  boolean  value.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Gets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never  null .

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined.

 **Remarks:** 

RK I have never seen this in use.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | char | The corresponding  char  value. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

This setting is purely a suggestion of the data source type that is being used for this mail merge.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/) constants. |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Sets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. This object is never  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is  false .

 **Remarks:** 

RK I have never seen this in use.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | A collection of objects that specify inclusion/exclusion of individual records in the mail merge. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

