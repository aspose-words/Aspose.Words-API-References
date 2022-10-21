---
title: MailMergeDataType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 382
url: /java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

A utility class providing constants. Specifies the type of an external mail merge data source.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No mail merge data source is specified. |
| [TEXT_FILE](#TEXT-FILE) | Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system. |
| [DATABASE](#DATABASE) | Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system. |
| [SPREADSHEET](#SPREADSHEET) | Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system. |
| [QUERY](#QUERY) | Specifies that a given document has been connected to an external data source using an external query tool. |
| [ODBC](#ODBC) | Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface. |
| [NATIVE](#NATIVE) | Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface. |
| [DEFAULT](#DEFAULT) | Equals to [NONE](../../com.aspose.words/mailmergedatatype\#NONE). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int mailMergeDataType)](#getName-int-) |  |
| [toString(int mailMergeDataType)](#toString-int-) |  |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No mail merge data source is specified.

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system.

### QUERY {#QUERY}
```
public static int QUERY
```


Specifies that a given document has been connected to an external data source using an external query tool.

### ODBC {#ODBC}
```
public static int ODBC
```


Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals to [NONE](../../com.aspose.words/mailmergedatatype\#NONE).

### length {#length}
```
public static int length
```


### getName(int mailMergeDataType) {#getName-int-}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### toString(int mailMergeDataType) {#toString-int-}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
