---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgenin orijinal veya revize edilmiş sürümüyle çalışılıp çalışılmayacağını belirtmeye olanak tanır."
type: docs
weight: 587
url: /tr/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Bir belgenin orijinal mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirtmeye olanak tanır.

 **Examples:** 

Bir belgenin revize edilmiş ve orijinal görünümü arasında nasıl geçiş yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FINAL](#FINAL) | Bir belgenin revize edilmiş sürümünü belirtir. |
| [ORIGINAL](#ORIGINAL) | Bir belgenin orijinal sürümünü belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Bir belgenin revize edilmiş sürümünü belirtir.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Bir belgenin orijinal sürümünü belirtir.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
