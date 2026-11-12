---
title: "ReadabilityStatistics"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words для Java"
description: "Предоставляет информацию о показателе удобочитаемости документа в Java."
type: docs
weight: 559
url: /ru/java/com.aspose.words/readabilitystatistics/
---

**Inheritance:**
java.lang.Object
```
public class ReadabilityStatistics
```

Предоставляет информацию о показателе читаемости документа.

 **Examples:** 

Показывает, как вычислять и отображать оценки чтения по Флешу для документа.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getFleschKincaidGradeLevel()](#getFleschKincaidGradeLevel) | Оценка уровня класса Флеш‑Кинкейда. |
| [getFleschReadingEasy()](#getFleschReadingEasy) | Оценка лёгкости чтения по Флеш. |
### getFleschKincaidGradeLevel() {#getFleschKincaidGradeLevel}
```
public double getFleschKincaidGradeLevel()
```


Оценка уровня класса Флеш‑Кинкейда.

**Returns:**
double - Соответствующее  double  значение.
### getFleschReadingEasy() {#getFleschReadingEasy}
```
public double getFleschReadingEasy()
```


Оценка лёгкости чтения по Флеш.

**Returns:**
double - Соответствующее  double  значение.
