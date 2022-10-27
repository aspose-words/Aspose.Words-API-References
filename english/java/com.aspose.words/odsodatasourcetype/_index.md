---
title: OdsoDataSourceType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of the external data source to be connected to as part of the ODSO connection information.
type: docs
weight: 412
url: /java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Specifies the type of the external data source to be connected to as part of the ODSO connection information.

The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Fields

| Field | Description |
| --- | --- |
| [TEXT](#TEXT) | Specifies that a given document has been connected to a text file. |
| [DATABASE](#DATABASE) | Specifies that a given document has been connected to a database. |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Specifies that a given document has been connected to an address book of contacts. |
| [DOCUMENT_1](#DOCUMENT-1) | Specifies that a given document has been connected to another document format supported by the producing application. |
| [DOCUMENT_2](#DOCUMENT-2) | Specifies that a given document has been connected to another document format supported by the producing application. |
| [NATIVE](#NATIVE) | Specifies that a given document has been connected to another document format native to the producing application. |
| [EMAIL](#EMAIL) | Specifies that a given document has been connected to an e-mail application. |
| [NONE](#NONE) | The type of the external data source is not specified. |
| [LEGACY](#LEGACY) | Specifies that a given document has been connected to a legacy document format supported by the producing application Possibly wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| [DEFAULT](#DEFAULT) | Equals to [NONE](../../com.aspose.words/odsodatasourcetype\#NONE). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int odsoDataSourceType)](#getName-int-) |  |
| [toString(int odsoDataSourceType)](#toString-int-) |  |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### TEXT {#TEXT}
```
public static int TEXT
```


Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess.

### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL.

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

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook.

### NONE {#NONE}
```
public static int NONE
```


The type of the external data source is not specified. Possibly wdMergeSubTypeWord.

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

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals to [NONE](../../com.aspose.words/odsodatasourcetype\#NONE).

### length {#length}
```
public static int length
```


### getName(int odsoDataSourceType) {#getName-int-}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### toString(int odsoDataSourceType) {#toString-int-}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
