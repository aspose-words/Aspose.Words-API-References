---
title: RelativeVerticalPosition
linktitle: RelativeVerticalPosition
second_title: Aspose.Words for Java
description: Specifies to what the vertical position of a shape or text frame is relative in Java.
type: docs
weight: 542
url: /java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Specifies to what the vertical position of a shape or text frame is relative.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Shows how to insert an image, and use it as a watermark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Specifies that the vertical positioning shall be relative to the bottom margin of the current page. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Specifies that the vertical positioning shall be relative to the inside margin of the current page. |
| [LINE](#LINE) | Undocumented. |
| [MARGIN](#MARGIN) | Specifies that the vertical positioning shall be relative to the page margins. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Specifies that the vertical positioning shall be relative to the outside margin of the current page. |
| [PAGE](#PAGE) | The object is positioned relative to the top edge of the page. |
| [PARAGRAPH](#PARAGRAPH) | The object is positioned relative to the top of the paragraph that contains the anchor. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | Default value is [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | Default value is [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Specifies that the vertical positioning shall be relative to the top margin of the current page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Specifies that the vertical positioning shall be relative to the bottom margin of the current page.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Specifies that the vertical positioning shall be relative to the inside margin of the current page.

### LINE {#LINE}
```
public static int LINE
```


Undocumented.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifies that the vertical positioning shall be relative to the page margins.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Specifies that the vertical positioning shall be relative to the outside margin of the current page.

### PAGE {#PAGE}
```
public static int PAGE
```


The object is positioned relative to the top edge of the page.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


The object is positioned relative to the top of the paragraph that contains the anchor.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


Default value is [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


Default value is [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Specifies that the vertical positioning shall be relative to the top margin of the current page.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
