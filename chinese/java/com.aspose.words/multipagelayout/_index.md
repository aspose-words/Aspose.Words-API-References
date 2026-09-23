---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words for Java"
description: "在 Java 中定义一种布局，用于将多个页面渲染为单个输出。"
type: docs
weight: 472
url: /zh/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

定义一种布局，用于将多个页面渲染为单个输出。

 **Remarks:** 

使用其中一个静态工厂方法来创建布局配置。

 **Examples:** 

展示如何使用多页布局设置将文档保存为 JPG 图像。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [getBackColor()](#getBackColor) | 获取输出的背景颜色。 |
| [getBorderColor()](#getBorderColor) | 获取页面边框的颜色。 |
| [getBorderWidth()](#getBorderWidth) | 获取页面边框的宽度。 |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | 创建一种布局，使页面按从左到右、从上到下的顺序在具有指定列数的网格中渲染。 |
| [horizontal(float horizontalGap)](#horizontal-float) | 创建一种布局，使所有指定页面水平并排、从左到右地在单个输出中渲染。 |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | 设置输出的背景颜色。 |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | 设置页面边框的颜色。 |
| [setBorderWidth(float value)](#setBorderWidth-float) | 设置页面边框的宽度。 |
| [singlePage()](#singlePage) | 创建一种布局，仅渲染指定页面中的第一页。 |
| [tiffFrames()](#tiffFrames) | 创建一种布局，使每个页面在多帧 TIFF 图像中渲染为单独的帧。 |
| [vertical(float verticalGap)](#vertical-float) | 创建一种布局，使所有指定页面在单个输出中垂直排列，一页接一页地渲染。 |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


获取输出的背景颜色。默认值为 java.awt.Color\\#EMPTY.EMPTY。

**Returns:**
java.awt.Color - 输出的背景颜色。
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


获取页面边框的颜色。默认值是 java.awt.Color\#EMPTY.EMPTY。

**Returns:**
java.awt.Color - 页面边框的颜色。
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


获取页面边框的宽度。默认值为 0。

**Returns:**
float - 页面边框的宽度。
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


创建一种布局，使页面按从左到右、从上到下的顺序在具有指定列数的网格中渲染。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 列 | int | 布局中的列数。必须大于零。 |
| horizontalGap | float | 列之间的水平间距（单位：点）。 |
| verticalGap | float | 行之间的垂直间距（单位：点）。 |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


创建一种布局，使所有指定页面水平并排、从左到右地在单个输出中渲染。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| horizontalGap | float | 页面之间的水平间距（单位：点）。 |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


设置输出的背景颜色。默认值是 java.awt.Color\#EMPTY.EMPTY。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 输出的背景颜色。 |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


设置页面边框的颜色。默认值是 java.awt.Color\#EMPTY.EMPTY。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 页面边框的颜色。 |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


设置页面边框的宽度。默认值为 0。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 页面边框的宽度。 |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


创建一种布局，仅渲染指定页面中的第一页。

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


创建一种布局，使每页在多帧 TIFF 图像中渲染为单独的帧。仅适用于 TIFF 图像格式。

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


创建一种布局，使所有指定页面在单个输出中垂直排列，一页接一页地渲染。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| verticalGap | float | 页面之间的垂直间距（单位：点）。 |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
