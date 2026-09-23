---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words für Java"
description: "Stellt Informationen über die Lesbarkeitsbewertung eines Dokuments in Java bereit."
type: docs
weight: 559
url: /de/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Stellt Informationen über die Lesbarkeitsbewertung eines Dokuments bereit.

 **Examples:** 

Zeigt, wie die Flesch‑Lesbarkeitswerte für ein Dokument berechnet und angezeigt werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Flesch‑Kincaid‑Klassenstufenscore. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Flesch‑Reading‑Easy‑Score. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Flesch‑Kincaid‑Klassenstufenscore.

**Returns:**
double - Der entsprechende  double  Wert.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Flesch‑Reading‑Easy‑Score.

**Returns:**
double - Der entsprechende  double  Wert.
