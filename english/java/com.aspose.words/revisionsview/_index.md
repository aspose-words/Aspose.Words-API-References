---
title: RevisionsView
linktitle: RevisionsView
second_title: Aspose.Words for Java
description: Allows to specify whether to work with the original or revised version of a document in Java.
type: docs
weight: 539
url: /java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Allows to specify whether to work with the original or revised version of a document.

 **Examples:** 

Shows how to switch between the revised and the original view of a document.

```

 Document doc = new Document(getMyDir() + "Revisions at list levels.docx");
 doc.updateListLabels();

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("1.", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("", paragraphs.get(2).getListLabel().getLabelString());

 // View the document object as if all the revisions are accepted. Currently supports list labels.
 doc.setRevisionsView(RevisionsView.FINAL);

 Assert.assertEquals("", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("1.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(2).getListLabel().getLabelString());
 
```
## Fields

| Field | Description |
| --- | --- |
| [FINAL](#FINAL) | Specifies revised version of a document. |
| [ORIGINAL](#ORIGINAL) | Specifies original version of a document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Specifies revised version of a document.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifies original version of a document.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int revisionsView) {#toString-int}
```
public static String toString(int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
