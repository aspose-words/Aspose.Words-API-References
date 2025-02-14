---
title: ViewType
linktitle: ViewType
second_title: Aspose.Words for Java
description: Possible values for the view mode in Microsoft Word in Java.
type: docs
weight: 690
url: /java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Possible values for the view mode in Microsoft Word.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | The document shall be rendered in the default view of the application. |
| [NORMAL](#NORMAL) | The document shall be rendered in a view optimized for outlining or creating long documents. |
| [OUTLINE](#OUTLINE) | The document shall be rendered in a view optimized for outlining or creating long documents. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | The document shall be opened in a view that displays the document as it will print. |
| [READING](#READING) | The document shall be rendered in the default view of the application. |
| [WEB](#WEB) | The document shall be rendered in a view mimicking the way this document would be displayed in a web page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


The document shall be rendered in the default view of the application.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


The document shall be rendered in a view optimized for outlining or creating long documents.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


The document shall be rendered in a view optimized for outlining or creating long documents.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


The document shall be opened in a view that displays the document as it will print.

### READING {#READING}
```
public static int READING
```


The document shall be rendered in the default view of the application.

### WEB {#WEB}
```
public static int WEB
```


The document shall be rendered in a view mimicking the way this document would be displayed in a web page.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
