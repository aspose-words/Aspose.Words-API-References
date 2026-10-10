---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words for Java"
description: "提供关于 Java 中文档可读性分数的信息。"
type: docs
weight: 559
url: /zh/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

提供关于文档可读性分数的信息。

 **Examples:** 

展示如何计算并显示文档的 Flesch 阅读分数。

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
 builder.writeln("Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
 builder.writeln("This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

 // Calculate readability statistics.
 ReadabilityStatistics stats = doc.getReadabilityStatistics();
 // Verify that the scores are within expected valid ranges.
 Assert.assertTrue(stats.getFleschReadingEasy() >= 0 && stats.getFleschReadingEasy() <= 190);
 Assert.assertTrue(stats.getFleschKincaidGradeLevel() <= 0);
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Flesch-Kincaid 年级水平分数。 |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Flesch 阅读易度分数。 |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Flesch-Kincaid 年级水平分数。

**Returns:**
double - 对应的 double 值。
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Flesch 阅读易度分数。

**Returns:**
double - 对应的 double 值。
