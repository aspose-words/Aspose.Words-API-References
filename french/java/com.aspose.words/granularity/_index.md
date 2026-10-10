---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words pour Java"
description: "Spécifie la granularité des modifications à suivre lors de la comparaison de deux documents en Java."
type: docs
weight: 366
url: /fr/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Spécifie la granularité des modifications à suivre lors de la comparaison de deux documents.

 **Examples:** 

Permet de spécifier une granularité lors de la comparaison de documents.

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
## Champs

| Champ | Description |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Spécifie les modifications au niveau des caractères. |
| [WORD_LEVEL](#WORD-LEVEL) | Spécifie les modifications au niveau du mot. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Spécifie les modifications au niveau des caractères.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Spécifie les modifications au niveau du mot.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
