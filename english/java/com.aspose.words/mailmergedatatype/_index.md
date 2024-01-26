---
title: MailMergeDataType
linktitle: MailMergeDataType
second_title: Aspose.Words for Java
description: Specifies the type of an external mail merge data source in Java.
type: docs
weight: 402
url: /java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Specifies the type of an external mail merge data source.
## Fields

| Field | Description |
| --- | --- |
| [DATABASE](#DATABASE) | Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system. |
| [DEFAULT](#DEFAULT) | Equals to [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface. |
| [NONE](#NONE) | No mail merge data source is specified. |
| [ODBC](#ODBC) | Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface. |
| [QUERY](#QUERY) | Specifies that a given document has been connected to an external data source using an external query tool. |
| [SPREADSHEET](#SPREADSHEET) | Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system. |
| [TEXT_FILE](#TEXT-FILE) | Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals to [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface.

### NONE {#NONE}
```
public static int NONE
```


No mail merge data source is specified.

### ODBC {#ODBC}
```
public static int ODBC
```


Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface.

### QUERY {#QUERY}
```
public static int QUERY
```


Specifies that a given document has been connected to an external data source using an external query tool.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system.

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDataType) {#toString-int}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
