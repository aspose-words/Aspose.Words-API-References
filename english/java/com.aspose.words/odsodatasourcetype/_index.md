---
title: OdsoDataSourceType
linktitle: OdsoDataSourceType
second_title: Aspose.Words for Java
description: Specifies the type of the external data source to be connected to as part of the ODSO connection information in Java.
type: docs
weight: 472
url: /java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Specifies the type of the external data source to be connected to as part of the ODSO connection information.

 **Remarks:** 

The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Fields

| Field | Description |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Specifies that a given document has been connected to an address book of contacts. |
| [DATABASE](#DATABASE) | Specifies that a given document has been connected to a database. |
| [DEFAULT](#DEFAULT) | Equals to [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Specifies that a given document has been connected to another document format supported by the producing application. |
| [DOCUMENT_2](#DOCUMENT-2) | Specifies that a given document has been connected to another document format supported by the producing application. |
| [EMAIL](#EMAIL) | Specifies that a given document has been connected to an e-mail application. |
| [LEGACY](#LEGACY) | Specifies that a given document has been connected to a legacy document format supported by the producing application Possibly wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| [NATIVE](#NATIVE) | Specifies that a given document has been connected to another document format native to the producing application. |
| [NONE](#NONE) | The type of the external data source is not specified. |
| [TEXT](#TEXT) | Specifies that a given document has been connected to a text file. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals to [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Specifies that a given document has been connected to a legacy document format supported by the producing application Possibly wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Specifies that a given document has been connected to a data source which aggregates other data sources.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


The type of the external data source is not specified. Possibly wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
