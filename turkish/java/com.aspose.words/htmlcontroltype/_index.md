---
title: "HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Aspose.Words Java için"
description: "HTML'den içe aktarılan  ve  öğelerini temsil eden belge düğümlerinin türü Java'da."
type: docs
weight: 377
url: /tr/java/com.aspose.words/htmlcontroltype/
---

**Inheritance:**
java.lang.Object
```
public class HtmlControlType
```

HTML'den içe aktarılan  ve  öğelerini temsil eden belge düğümlerinin türü. Örnekler: İçe aktarılan  ve  öğelerini temsil edecek tercih edilen belge düğümü tipinin nasıl ayarlanacağını gösterir.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FORM_FIELD](#FORM-FIELD) | Bir form alanı. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Yapılandırılmış belge etiketi |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String htmlControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int htmlControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlControlType)](#toString-int) |  |
### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Bir form alanı.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Yapılandırılmış belge etiketi

### length {#length}
```
public static int length
```


### fromName(String htmlControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlControlTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlControlType) {#getName-int}
```
public static String getName(int htmlControlType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
