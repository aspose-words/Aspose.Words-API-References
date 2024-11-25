---
title: RelativeHorizontalPosition
linktitle: RelativeHorizontalPosition
second_title: Aspose.Words for Java
description: Specifies to what the horizontal position of a shape or text frame is relative in Java.
type: docs
weight: 532
url: /java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Specifies to what the horizontal position of a shape or text frame is relative.

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
| [CHARACTER](#CHARACTER) | The object is positioned relative to the left side of the paragraph. |
| [COLUMN](#COLUMN) | The object is positioned relative to the left side of the column. |
| [DEFAULT](#DEFAULT) | Default value is [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Specifies that the horizontal positioning shall be relative to the inside margin of the current page (the left margin on odd pages, right on even pages). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Specifies that the horizontal positioning shall be relative to the left margin of the page. |
| [MARGIN](#MARGIN) | Specifies that the horizontal positioning shall be relative to the page margins. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Specifies that the horizontal positioning shall be relative to the outside margin of the current page (the right margin on odd pages, left on even pages). |
| [PAGE](#PAGE) | The object is positioned relative to the left edge of the page. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Specifies that the horizontal positioning shall be relative to the right margin of the page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


The object is positioned relative to the left side of the paragraph.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


The object is positioned relative to the left side of the column.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Specifies that the horizontal positioning shall be relative to the inside margin of the current page (the left margin on odd pages, right on even pages).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Specifies that the horizontal positioning shall be relative to the left margin of the page.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifies that the horizontal positioning shall be relative to the page margins.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Specifies that the horizontal positioning shall be relative to the outside margin of the current page (the right margin on odd pages, left on even pages).

### PAGE {#PAGE}
```
public static int PAGE
```


The object is positioned relative to the left edge of the page.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Specifies that the horizontal positioning shall be relative to the right margin of the page.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
