---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words para Java"
description: "Proporciona información sobre la puntuación de legibilidad del documento en Java."
type: docs
weight: 559
url: /es/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Proporciona información sobre la puntuación de legibilidad del documento.

 **Examples:** 

Muestra cómo calcular y mostrar las puntuaciones de lectura Flesch para un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Puntuación de nivel de grado Flesch-Kincaid. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Puntuación de lectura fácil Flesch. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Puntuación de nivel de grado Flesch-Kincaid.

**Returns:**
double - El valor  double  correspondiente.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Puntuación de lectura fácil Flesch.

**Returns:**
double - El valor  double  correspondiente.
