---
title: ReadabilityStatistics
linktitle: ReadabilityStatistics
second_title: Aspose.Words for Java
description: Provides information about document readability score in Java.
type: docs
weight: 559
url: /java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Provides information about document readability score.

 **Examples:** 

Shows how to calculate and display the Flesch reading scores for a document.

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
## Methods

| Method | Description |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Flesch-Kincaid Grade Level score. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Flesch Reading Easy score. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Flesch-Kincaid Grade Level score.

**Returns:**
double - The corresponding  double  value.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Flesch Reading Easy score.

**Returns:**
double - The corresponding  double  value.
