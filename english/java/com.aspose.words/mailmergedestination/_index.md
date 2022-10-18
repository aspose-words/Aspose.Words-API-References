---
title: MailMergeDestination
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 383
url: /java/com.aspose.words/mailmergedestination/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDestination
```

A utility class providing constants. Specifies the possible results which may be generated when a mail merge is carried out on a document.
## Fields

| Field | Description |
| --- | --- |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | Specifies that conforming hosting applications shall generate new documents by populating the fields within a given document with data from the specified external data source. |
| [PRINTER](#PRINTER) | Specifies that conforming hosting applications shall print the documents that result from populating the fields within a given document with external data from the specified external data source. |
| [EMAIL](#EMAIL) | Specifies that conforming hosting applications shall generate emails using the documents that result from populating the fields within a given document with data from the specified external data source. |
| [FAX](#FAX) | Specifies that conforming hosting applications shall generate faxes using the documents that result from populating the fields within a given document with data from the specified external data source. |
| [DEFAULT](#DEFAULT) | Equals to the [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination\#NEW-DOCUMENT) value. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int mailMergeDestination)](#getName-int-) |  |
| [toString(int mailMergeDestination)](#toString-int-) |  |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


Specifies that conforming hosting applications shall generate new documents by populating the fields within a given document with data from the specified external data source.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


Specifies that conforming hosting applications shall print the documents that result from populating the fields within a given document with external data from the specified external data source.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Specifies that conforming hosting applications shall generate emails using the documents that result from populating the fields within a given document with data from the specified external data source.

### FAX {#FAX}
```
public static int FAX
```


Specifies that conforming hosting applications shall generate faxes using the documents that result from populating the fields within a given document with data from the specified external data source.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals to the [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination\#NEW-DOCUMENT) value.

### length {#length}
```
public static int length
```


### getName(int mailMergeDestination) {#getName-int-}
```
public static String getName(int mailMergeDestination)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### toString(int mailMergeDestination) {#toString-int-}
```
public static String toString(int mailMergeDestination)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### fromName(String mailMergeDestinationName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeDestinationName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
