---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Angabe, ob in Java mit der Original‑ oder der überarbeiteten Version eines Dokuments gearbeitet werden soll."
type: docs
weight: 587
url: /de/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Ermöglicht die Angabe, ob mit der Original- oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

 **Examples:** 

Zeigt, wie man zwischen der überarbeiteten und der Originalansicht eines Dokuments wechselt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FINAL](#FINAL) | Gibt die überarbeitete Version eines Dokuments an. |
| [ORIGINAL](#ORIGINAL) | Gibt die Originalversion eines Dokuments an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Gibt die überarbeitete Version eines Dokuments an.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Gibt die Originalversion eines Dokuments an.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
