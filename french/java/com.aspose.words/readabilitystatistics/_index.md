---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words pour Java"
description: "Fournit des informations sur le score de lisibilité d’un document en Java."
type: docs
weight: 559
url: /fr/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Fournit des informations sur le score de lisibilité du document.

 **Examples:** 

Montre comment calculer et afficher les scores de lecture Flesch pour un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Score de niveau de classe Flesch‑Kincaid. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Score de lecture facile Flesch. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Score de niveau de classe Flesch‑Kincaid.

**Returns:**
double - La valeur  double  correspondante.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Score de lecture facile Flesch.

**Returns:**
double - La valeur  double  correspondante.
