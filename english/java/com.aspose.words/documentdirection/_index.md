---
title: DocumentDirection
linktitle: DocumentDirection
second_title: Aspose.Words for Java
description: Allows to specify the direction to flow the text in a document in Java.
type: docs
weight: 151
url: /java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Allows to specify the direction to flow the text in a document.

 **Examples:** 

Shows how to detect plaintext document text direction.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Auto-detect direction. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Left to right direction. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Right to left direction. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Auto-detect direction.

 **Remarks:** 

When this option is selected and text contains characters belonging to RTL scripts, the document direction will be set automatically to RTL.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Left to right direction.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Right to left direction.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentDirection) {#toString-int}
```
public static String toString(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
