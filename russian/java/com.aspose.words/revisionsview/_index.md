---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words для Java"
description: "Позволяет указать, работать ли с оригинальной или исправленной версией документа в Java."
type: docs
weight: 587
url: /ru/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Позволяет указать, работать ли с оригинальной или изменённой версией документа.

 **Examples:** 

Показывает, как переключаться между исправленным и оригинальным представлением документа.

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
## Поля

| Поле | Описание |
| --- | --- |
| [FINAL](#FINAL) | Указывает исправленную версию документа. |
| [ORIGINAL](#ORIGINAL) | Указывает оригинальную версию документа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Указывает исправленную версию документа.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Указывает оригинальную версию документа.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
