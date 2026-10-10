---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words for Java"
description: "指定 Java 中字体在行上的垂直位置。"
type: docs
weight: 36
url: /zh/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

指定字体在行上的垂直位置。

 **Examples:** 

展示如何设置字体在行上的垂直位置。

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 基线会自动调整。 |
| [BASELINE](#BASELINE) | 对齐到段落的基线。 |
| [BOTTOM](#BOTTOM) | 对齐到每个字体的底部。 |
| [CENTER](#CENTER) | 对齐每个字体的中心点。 |
| [TOP](#TOP) | 对齐到每个字体的顶部。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


基线会自动调整。

### BASELINE {#BASELINE}
```
public static int BASELINE
```


对齐到段落的基线。

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


对齐到每个字体的底部。

### CENTER {#CENTER}
```
public static int CENTER
```


对齐每个字体的中心点。

### TOP {#TOP}
```
public static int TOP
```


对齐到每个字体的顶部。

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int baselineAlignment) {#toString-int}
```
public static String toString(int baselineAlignment)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
