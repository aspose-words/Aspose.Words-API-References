---
title: ZoomType
linktitle: ZoomType
second_title: Aspose.Words for Java
description: Possible values for how large or small the document appears on the screen in Microsoft Word in Java.
type: docs
weight: 746
url: /java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Possible values for how large or small the document appears on the screen in Microsoft Word.

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
| [CUSTOM](#CUSTOM) | Zoom percentage is set explicitly. |
| [FULL_PAGE](#FULL-PAGE) | Zoom percentage is automatically recalculated to fit one full page. |
| [NONE](#NONE) | Indicates to use the explicit zoom percentage. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Zoom percentage is automatically recalculated to fit page width. |
| [TEXT_FIT](#TEXT-FIT) | Zoom percentage is automatically recalculated to fit text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Zoom percentage is set explicitly. It is not recalculated automatically when control size changes.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Zoom percentage is automatically recalculated to fit one full page.

### NONE {#NONE}
```
public static int NONE
```


Indicates to use the explicit zoom percentage. Same as [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Zoom percentage is automatically recalculated to fit page width.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Zoom percentage is automatically recalculated to fit text.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
