---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words لـ Java"
description: "يحدد مظهر علامة المستند المُنظم في جافا."
type: docs
weight: 599
url: /ar/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

يحدد مظهر علامة المستند المهيكلة.

 **Examples:** 

يوضح كيفية إظهار العلامة حول المحتوى.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | يمثل علامة مستند مُنظم تُعرض كمستطيل مُظلَل أو صندوق حدود. |
| [DEFAULT](#DEFAULT) | الافتراضي هو [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | يمثل علامة مستند مُنظم غير معروضة. |
| [TAGS](#TAGS) | يمثل علامة مستند مُنظم تُعرض كعلامات بداية ونهاية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


يمثل علامة مستند مُنظم تُعرض كمستطيل مُظلَل أو صندوق حدود.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


الافتراضي هو [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


يمثل علامة مستند مُنظم غير معروضة.

### TAGS {#TAGS}
```
public static int TAGS
```


يمثل علامة مستند مُنظم تُعرض كعلامات بداية ونهاية.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtAppearance) {#toString-int}
```
public static String toString(int sdtAppearance)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
