---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words para Java"
description: "Especifica la granularidad de los cambios a rastrear al comparar dos documentos en Java."
type: docs
weight: 366
url: /es/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Especifica la granularidad de los cambios a rastrear al comparar dos documentos.

 **Examples:** 

Muestra cómo especificar una granularidad al comparar documentos.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Especifica cambios a nivel de carácter. |
| [WORD_LEVEL](#WORD-LEVEL) | Especifica cambios a nivel de palabra. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Especifica cambios a nivel de carácter.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Especifica cambios a nivel de palabra.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
