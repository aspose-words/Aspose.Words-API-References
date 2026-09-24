---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words Java için"
description: "Java'da belge okunabilirlik puanı hakkında bilgi sağlar."
type: docs
weight: 559
url: /tr/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Belge okunabilirlik puanı hakkında bilgi sağlar.

 **Examples:** 

Bir belge için Flesch okuma puanlarını nasıl hesaplayıp görüntüleyeceğinizi gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Flesch-Kincaid Sınıf Seviyesi puanı. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Flesch Okuma Kolaylığı puanı. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Flesch-Kincaid Sınıf Seviyesi puanı.

**Returns:**
double - İlgili  double  değeri.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Flesch Okuma Kolaylığı puanı.

**Returns:**
double - İlgili  double  değeri.
