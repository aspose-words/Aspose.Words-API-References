---
title: "RevisionsView"
linktitle: "RevisionsView"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد ما إذا كان سيتم العمل بالإصدار الأصلي أو الإصدار المعدل من المستند في Java."
type: docs
weight: 587
url: /ar/java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

يسمح بتحديد ما إذا كان سيتم العمل بالإصدار الأصلي أو المعدَّل من المستند.

 **Examples:** 

يوضح كيفية التبديل بين العرض المعدل والعرض الأصلي للمستند.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FINAL](#FINAL) | يحدد الإصدار المعدل من المستند. |
| [ORIGINAL](#ORIGINAL) | يحدد الإصدار الأصلي من المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionsView)](#toString-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


يحدد الإصدار المعدل من المستند.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


يحدد الإصدار الأصلي من المستند.

### length {#length}
```
public static int length
```


### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionsView | int |  |

**Returns:**
java.lang.String
