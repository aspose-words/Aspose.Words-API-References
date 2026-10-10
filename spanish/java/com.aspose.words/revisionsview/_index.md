---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words para Java"
description: "Permite especificar si trabajar con la versión original o revisada de un documento en Java."
type: docs
weight: 587
url: /es/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Permite especificar si se trabaja con la versión original o revisada de un documento.

 **Examples:** 

Muestra cómo cambiar entre la vista revisada y la vista original de un documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FINAL](#FINAL) | Especifica la versión revisada de un documento. |
| [ORIGINAL](#ORIGINAL) | Especifica la versión original de un documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Especifica la versión revisada de un documento.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Especifica la versión original de un documento.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
