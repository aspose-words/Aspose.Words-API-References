---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words for Java"
description: "指定文档在 Java 中如何拆分为多个部分的选项。"
type: docs
weight: 630
url: /zh/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

指定文档如何拆分为多个部分的选项。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | 指定将文档拆分为多个部分的标准。 |
| [getSplitStyle()](#getSplitStyle) | 指定在使用 [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\\#STYLE) 时用于拆分文档为多个部分的段落样式。 |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | 指定将文档拆分为多个部分的标准。 |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | 指定在使用 [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\\#STYLE) 时用于拆分文档为多个部分的段落样式。 |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


指定将文档拆分为多个部分的标准。

 **Examples:** 

展示如何按页拆分文档。

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - 对应的 int 值。返回值是 [SplitCriteria](../../com.aspose.words/splitcriteria/) 常量之一。
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


指定在使用 [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\\#STYLE) 时用于拆分文档为多个部分的段落样式。

**Returns:**
java.lang.String - 相应的 java.lang.String 值。
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


指定将文档拆分为多个部分的标准。

 **Examples:** 

展示如何按页拆分文档。

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是 [SplitCriteria](../../com.aspose.words/splitcriteria/) 常量之一。 |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


指定在使用 [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\\#STYLE) 时用于拆分文档为多个部分的段落样式。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

