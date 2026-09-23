---
title: "MustacheTag"
linktitle: "MustacheTag"
second_title: "Aspose.Words for Java"
description: "表示 Java 中的 Mustache 标记。"
type: docs
weight: 474
url: /zh/java/com.aspose.words/mustachetag/
---

**Inheritance:**
java.lang.Object
```
public class MustacheTag
```

表示 “mustache” 标记。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getReferenceOffset()](#getReferenceOffset) | 获取标签相对于 [getReferenceRun()](../../com.aspose.words/mustachetag/\#getReferenceRun) 开始处的零基起始位置。 |
| [getReferenceRun()](#getReferenceRun) | 获取包含标签起始位置的运行。 |
| [getText()](#getText) | 获取标签的文本。 |
### getReferenceOffset() {#getReferenceOffset}
```
public int getReferenceOffset()
```


获取标签相对于 [getReferenceRun()](../../com.aspose.words/mustachetag/\#getReferenceRun) 开始处的零基起始位置。

**Returns:**
int - 标签相对于 [getReferenceRun()](../../com.aspose.words/mustachetag/\#getReferenceRun) 开始处的零基起始位置。
### getReferenceRun() {#getReferenceRun}
```
public Run getReferenceRun()
```


获取包含标签起始位置的运行。

**Returns:**
[Run](../../com.aspose.words/run/) - The run that contains the beginning of the tag.
### getText() {#getText}
```
public String getText()
```


获取标签的文本。

**Returns:**
java.lang.String - 标签的文本。
