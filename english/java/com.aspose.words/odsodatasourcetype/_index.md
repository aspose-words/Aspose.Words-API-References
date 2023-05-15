---
title: OdsoDataSourceType
linktitle: OdsoDataSourceType
second_title: Aspose.Words for Java
description: Specifies the type of the external data source to be connected to as part of the ODSO connection information in Java.
type: docs
weight: 429
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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

