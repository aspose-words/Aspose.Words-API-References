---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words لـ Java"
description: "يوفر معلومات حول درجة قابلية قراءة المستند في Java."
type: docs
weight: 559
url: /ar/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

يوفر معلومات حول درجة قابلية قراءة المستند.

 **Examples:** 

يوضح كيفية حساب وعرض درجات قراءة فليش لمستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | درجة مستوى الصف فليش-كينكيد. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | درجة قراءة فليش السهلة. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


درجة مستوى الصف فليش-كينكيد.

**Returns:**
double - القيمة المقابلة للـ double.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


درجة قراءة فليش السهلة.

**Returns:**
double - القيمة المقابلة للـ double.
