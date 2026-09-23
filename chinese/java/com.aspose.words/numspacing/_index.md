---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中数字间距可以显示的可能值。"
type: docs
weight: 484
url: /zh/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

指定数字间距可以显示的可能值。

 **Examples:** 

展示如何设置数字的间距类型。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [DEFAULT](#DEFAULT) | 指定数字以字体的默认形式显示。 |
| [PROPORTIONAL](#PROPORTIONAL) | 指定如果字体支持，则以比例间距的形式显示数字。 |
| [TABULAR](#TABULAR) | 指定如果字体支持，则以等宽（表格）形式显示数字。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


指定数字以字体的默认形式显示。

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


指定如果字体支持，则以比例间距的形式显示数字。

### TABULAR {#TABULAR}
```
public static int TABULAR
```


指定如果字体支持，则以等宽（表格）形式显示数字。

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
