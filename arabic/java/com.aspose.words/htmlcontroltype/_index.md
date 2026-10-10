---
title: "HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Aspose.Words لـ Java"
description: "نوع عقد المستند التي تمثل عناصر  و  المستوردة من HTML في Java."
type: docs
weight: 377
url: /ar/java/com.aspose.words/htmlcontroltype/
---

**Inheritance:**
java.lang.Object
```
public class HtmlControlType
```

نوع عقد المستند التي تمثل عناصر  و  المستوردة من HTML. أمثلة: يوضح كيفية تعيين النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و .   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);
## الحقول

| حقل | الوصف |
| --- | --- |
| [FORM_FIELD](#FORM-FIELD) | حقل نموذج. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | علامة مستند منسقة |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String htmlControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int htmlControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlControlType)](#toString-int) |  |
### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


حقل نموذج.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


علامة مستند منسقة

### length {#length}
```
public static int length
```


### fromName(String htmlControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlControlTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlControlType) {#getName-int}
```
public static String getName(int htmlControlType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlControlType) {#toString-int}
```
public static String toString(int htmlControlType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
