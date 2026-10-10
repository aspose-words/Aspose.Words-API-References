---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words für Java"
description: "Gibt die Granularität der Änderungen an, die beim Vergleich von zwei Dokumenten in Java verfolgt werden sollen."
type: docs
weight: 366
url: /de/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich zweier Dokumente an.

 **Examples:** 

Zeigt, wie man eine Granularität beim Vergleich von Dokumenten angibt.

```

 Document docA = new Document();
 DocumentBuilder builderA = new DocumentBuilder(docA);
 builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

 Document docB = new Document();
 DocumentBuilder builderB = new DocumentBuilder(docB);
 builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

 // Specify whether changes are tracking
 // by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setGranularity(granularity);

 docA.compare(docB, "author", new Date(), compareOptions);

 // The first document's collection of revision groups contains all the differences between documents.
 RevisionGroupCollection groups = docA.getRevisions().getGroups();
 Assert.assertEquals(5, groups.getCount());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Gibt Änderungen auf Zeichenebene an. |
| [WORD_LEVEL](#WORD-LEVEL) | Gibt Änderungen auf Wortebene an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Gibt Änderungen auf Zeichenebene an.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Gibt Änderungen auf Wortebene an.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int granularity) {#toString-int}
```
public static String toString(int granularity)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
