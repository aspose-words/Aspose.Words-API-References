---
title: HtmlControlType
linktitle: HtmlControlType
second_title: Aspose.Words for Java
description: Type of document nodes that represent  and  elements imported from HTML in Java.
type: docs
weight: 356
url: /java/com.aspose.words/htmlcontroltype/
---

**Inheritance:**
java.lang.Object
```
public class HtmlControlType
```

Type of document nodes that represent  and  elements imported from HTML. Examples:Shows how to set preferred type of document nodes that will represent imported  and  elements.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0); 
## Fields

| Field | Description |
| --- | --- |
| [FORM_FIELD](#FORM-FIELD) | A form field. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | A structured document tag |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String htmlControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int htmlControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlControlType)](#toString-int) |  |
### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


A form field.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


A structured document tag

### length {#length}
```
public static int length
```


### fromName(String htmlControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlControlTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlControlType) {#getName-int}
```
public static String getName(int htmlControlType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlControlType) {#toString-int}
```
public static String toString(int htmlControlType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
