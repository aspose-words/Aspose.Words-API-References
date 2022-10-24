---
title: ContentDisposition
second_title: Aspose.Words for Java API Reference
description: Enumerates different ways of presenting the document at the client browser.
type: docs
weight: 92
url: /java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumerates different ways of presenting the document at the client browser.

Note that the actual behavior on the client browser might be affected by security configuration of the browser.
## Fields

| Field | Description |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| [INLINE](#INLINE) | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int contentDisposition)](#getName-int-) |  |
| [toString(int contentDisposition)](#toString-int-) |  |
| [fromName(String contentDispositionName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension.

### INLINE {#INLINE}
```
public static int INLINE
```


Send the document to the browser and presents an option to save the document to disk or open inside the browser.

### length {#length}
```
public static int length
```


### getName(int contentDisposition) {#getName-int-}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### toString(int contentDisposition) {#toString-int-}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### fromName(String contentDispositionName) {#fromName-java.lang.String-}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
