---
title: ContentDisposition
linktitle: ContentDisposition
second_title: Aspose.Words for Java
description: Enumerates different ways of presenting the document at the client browser in Java.
type: docs
weight: 107
url: /java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumerates different ways of presenting the document at the client browser.

 **Remarks:** 

Note that the actual behavior on the client browser might be affected by security configuration of the browser.

 **Examples:** 

Shows how to perform a mail merge, and then save the document to the client browser.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Fields

| Field | Description |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| [INLINE](#INLINE) | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
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


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
