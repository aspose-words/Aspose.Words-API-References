---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words per Java"
description: "Consente di specificare se lavorare con la versione originale o revisionata di un documento in Java."
type: docs
weight: 587
url: /it/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Consente di specificare se lavorare con la versione originale o revisionata di un documento.

 **Examples:** 

Mostra come passare dalla visualizzazione revisionata a quella originale di un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FINAL](#FINAL) | Specifica la versione revisionata di un documento. |
| [ORIGINAL](#ORIGINAL) | Specifica la versione originale di un documento. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Specifica la versione revisionata di un documento.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifica la versione originale di un documento.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
