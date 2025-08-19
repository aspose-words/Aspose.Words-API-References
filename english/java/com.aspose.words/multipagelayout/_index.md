---
title: MultiPageLayout
linktitle: MultiPageLayout
second_title: Aspose.Words for Java
description: Defines a layout for rendering multiple pages into a single output in Java.
type: docs
weight: 467
url: /java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Defines a layout for rendering multiple pages into a single output.

 **Remarks:** 

Use one of the static factory methods to create a layout configuration.

 **Examples:** 

Shows how to save the document into JPG image with multi-page layout settings.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Methods

| Method | Description |
| --- | --- |
| [getBackColor()](#getBackColor) | Gets the background color of the output. |
| [getBorderColor()](#getBorderColor) | Gets the color of the pages border. |
| [getBorderWidth()](#getBorderWidth) | Gets the width of the pages border. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns. |
| [horizontal(float horizontalGap)](#horizontal-float) | Creates a layout in which all specified pages are rendered horizontally side by side, left to right, in a single output. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Sets the background color of the output. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Sets the color of the pages border. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Sets the width of the pages border. |
| [singlePage()](#singlePage) | Creates a layout that renders only the first of specified pages. |
| [tiffFrames()](#tiffFrames) | Creates a layout where each page is rendered as a separate frame in a multi-frame TIFF image. |
| [vertical(float verticalGap)](#vertical-float) | Creates a layout where all specified pages are rendered vertically one below the other in a single output. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Gets the background color of the output. The default is java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - The background color of the output.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Gets the color of the pages border. The default is java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - The color of the pages border.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Gets the width of the pages border. The default is 0.

**Returns:**
float - The width of the pages border.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columns | int | The number of columns in the layout. Must be greater than zero. |
| horizontalGap | float | The horizontal gap between columns in points. |
| verticalGap | float | The vertical gap between rows in points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Creates a layout in which all specified pages are rendered horizontally side by side, left to right, in a single output.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalGap | float | The horizontal gap between pages in points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Sets the background color of the output. The default is java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The background color of the output. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Sets the color of the pages border. The default is java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the pages border. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Sets the width of the pages border. The default is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The width of the pages border. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Creates a layout that renders only the first of specified pages.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Creates a layout where each page is rendered as a separate frame in a multi-frame TIFF image. Applicable only to TIFF image formats.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Creates a layout where all specified pages are rendered vertically one below the other in a single output.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| verticalGap | float | The vertical gap between pages in points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
