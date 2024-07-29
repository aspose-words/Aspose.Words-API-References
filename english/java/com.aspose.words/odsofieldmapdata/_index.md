---
title: OdsoFieldMapData
linktitle: OdsoFieldMapData
second_title: Aspose.Words for Java
description: Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document in Java.
type: docs
weight: 453
url: /java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

Microsoft Word provides some predefined merge field names that it allows to insert into a document as MERGEFIELD or use in the ADDRESSBLOCK or GREETINGLINE fields. The information specified in [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) allows to map one column in the external data source to a single predefined merge field.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Returns a deep clone of this object. |
| [getColumn()](#getColumn) | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. |
| [getMappedName()](#getMappedName) | Specifies the predefined merge field name which shall be mapped to the column number specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property within this field mapping. |
| [getName()](#getName) | Specifies the column name within an external data source for the column whose index is specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property. |
| [getType()](#getType) | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. |
| [setColumn(int value)](#setColumn-int) | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Specifies the predefined merge field name which shall be mapped to the column number specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property within this field mapping. |
| [setName(String value)](#setName-java.lang.String) | Specifies the column name within an external data source for the column whose index is specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property. |
| [setType(int value)](#setType-int) | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Returns a deep clone of this object.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Specifies the predefined merge field name which shall be mapped to the column number specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property within this field mapping. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getName() {#getName}
```
public String getName()
```


Specifies the column name within an external data source for the column whose index is specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property. The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getType() {#getType}
```
public int getType()
```


Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) constants.
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Specifies the predefined merge field name which shall be mapped to the column number specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property within this field mapping. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Specifies the column name within an external data source for the column whose index is specified by the [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) property. The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) constants. |

