---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier s’il faut travailler avec la version originale ou révisée d’un document en Java."
type: docs
weight: 587
url: /fr/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Permet de spécifier s'il faut travailler avec la version originale ou révisée d'un document.

 **Examples:** 

Montre comment basculer entre la vue révisée et la vue originale d’un document.

```

 Document doc = new Document(getMyDir() + "Revisions at list levels.docx");
 doc.updateListLabels();

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("1.", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("", paragraphs.get(2).getListLabel().getLabelString());

 // View the document object as if all the revisions are accepted. Currently supports list labels.
 doc.setRevisionsView(RevisionsView.FINAL);

 Assert.assertEquals("", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("1.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(2).getListLabel().getLabelString());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [FINAL](#FINAL) | Spécifie la version révisée d’un document. |
| [ORIGINAL](#ORIGINAL) | Spécifie la version originale d’un document. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Spécifie la version révisée d’un document.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Spécifie la version originale d’un document.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int revisionsView) {#toString-int}
```
public static String toString(int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
