---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中使用 PDF 阅读器打开文档时的页面布局。"
type: docs
weight: 539
url: /zh/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

指定在 PDF 阅读器打开文档时使用的页面布局。

 **Examples:** 

展示在 PDF 阅读器中打开时如何显示页面。

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | 以单列显示页面。 |
| [SINGLE_PAGE](#SINGLE-PAGE) | 一次显示一页。 |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | 以两列显示页面，奇数页在左侧。 |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | 以两列显示页面，奇数页在右侧。 |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | 一次显示两页，奇数页在左侧。 |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | 一次显示两页，奇数页在右侧。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


以单列显示页面。

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


一次显示一页。

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


以两列显示页面，奇数页在左侧。

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


以两列显示页面，奇数页在右侧。

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


一次显示两页，奇数页在左侧。

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


一次显示两页，奇数页在右侧。

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageLayout) {#toString-int}
```
public static String toString(int pdfPageLayout)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
