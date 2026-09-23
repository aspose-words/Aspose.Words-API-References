---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words for Java"
description: "提供 Java 中合并运行操作的配置标志。"
type: docs
weight: 406
url: /zh/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

提供合并运行操作的配置标志。

 **Examples:** 

展示如何在忽略冗余和不重要属性的情况下合并具有相同格式的运行。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True 表示在合并具有相同格式的运行时，将忽略所有运行的不重要属性。 |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True 表示在合并具有相同格式的运行时，将忽略所有运行的冗余属性。 |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True 表示在合并具有相同格式的运行时，将忽略所有运行的间距属性。 |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True 表示在合并具有相同格式的运行时，将忽略所有运行的不重要属性。 |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True 表示在合并具有相同格式的运行时，将忽略所有运行的冗余属性。 |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True 表示在合并具有相同格式的运行时，将忽略所有运行的间距属性。 |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的不重要属性。

 **Remarks:** 

不重要属性是指对具有给定文本内容的运行的格式没有显著影响的属性。默认值为 False。

**Returns:**
boolean - 相应的 boolean 值。
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的冗余属性。

 **Remarks:** 

冗余属性是指对具有给定文本内容的运行没有影响的属性。默认值为 False。

**Returns:**
boolean - 相应的 boolean 值。
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的间距属性。

 **Remarks:** 

默认值为 False。

**Returns:**
boolean - 相应的 boolean 值。
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的不重要属性。

 **Remarks:** 

不重要属性是指对具有给定文本内容的运行的格式没有显著影响的属性。默认值为 False。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的冗余属性。

 **Remarks:** 

冗余属性是指对具有给定文本内容的运行没有影响的属性。默认值为 False。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True 表示在合并具有相同格式的运行时，将忽略所有运行的间距属性。

 **Remarks:** 

默认值为 False。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

