---
title: Margins
linktitle: Margins
second_title: Aspose.Words for Java
description: Specifies preset margins in Java.
type: docs
weight: 426
url: /java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Specifies preset margins.

 **Examples:** 

Shows when to recalculate the page layout of the document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CUSTOM](#CUSTOM) | Custom margins. |
| [MIRRORED](#MIRRORED) | Mirrored margins. |
| [MODERATE](#MODERATE) | Moderate margins. |
| [NARROW](#NARROW) | Narrow margins. |
| [NORMAL](#NORMAL) | Normal margins. |
| [WIDE](#WIDE) | Wide margins. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Custom margins.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Mirrored margins.

 **Remarks:** 

Setting margins to Mirrored will set the appropriate value for [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int) property. This will affect the whole document, not just the current section.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Moderate margins.

### NARROW {#NARROW}
```
public static int NARROW
```


Narrow margins.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal margins.

### WIDE {#WIDE}
```
public static int WIDE
```


Wide margins.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
