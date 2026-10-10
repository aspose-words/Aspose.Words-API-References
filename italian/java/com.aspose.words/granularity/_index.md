---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words per Java"
description: "Specifica la granularità delle modifiche da tenere traccia durante il confronto di due documenti in Java."
type: docs
weight: 366
url: /it/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Specifica la granularità delle modifiche da tracciare durante il confronto di due documenti.

 **Examples:** 

Mostra come specificare una granularità durante il confronto dei documenti.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Specifica le modifiche a livello di carattere. |
| [WORD_LEVEL](#WORD-LEVEL) | Specifica le modifiche a livello di parola. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Specifica le modifiche a livello di carattere.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Specifica le modifiche a livello di parola.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
