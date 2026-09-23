---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words per Java"
description: "Fornisce informazioni sul punteggio di leggibilità del documento in Java."
type: docs
weight: 559
url: /it/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Fornisce informazioni sul punteggio di leggibilità del documento.

 **Examples:** 

Mostra come calcolare e visualizzare i punteggi di lettura Flesch per un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Punteggio del livello di classe Flesch‑Kincaid. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Punteggio di lettura facile Flesch. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Punteggio del livello di classe Flesch‑Kincaid.

**Returns:**
double - Il valore double corrispondente.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Punteggio di lettura facile Flesch.

**Returns:**
double - Il valore double corrispondente.
