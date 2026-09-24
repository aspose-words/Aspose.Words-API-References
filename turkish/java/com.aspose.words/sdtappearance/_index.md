---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words Java için"
description: "Java'da yapılandırılmış belge etiketi görünümünü belirtir."
type: docs
weight: 599
url: /tr/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Yapılandırılmış belge etiketinin görünümünü belirtir.

 **Examples:** 

İçeriğin etrafında etiketi nasıl göstereceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Gölgelendirilmiş bir dikdörtgen veya sınırlayıcı kutu olarak gösterilen bir yapılandırılmış belge etiketini temsil eder. |
| [DEFAULT](#DEFAULT) | Varsayılan olarak [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX) olur. |
| [HIDDEN](#HIDDEN) | Görünmeyen bir yapılandırılmış belge etiketini temsil eder. |
| [TAGS](#TAGS) | Başlangıç ve bitiş işaretleri olarak gösterilen bir yapılandırılmış belge etiketini temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Gölgelendirilmiş bir dikdörtgen veya sınırlayıcı kutu olarak gösterilen bir yapılandırılmış belge etiketini temsil eder.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan olarak [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX) olur.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Görünmeyen bir yapılandırılmış belge etiketini temsil eder.

### TAGS {#TAGS}
```
public static int TAGS
```


Başlangıç ve bitiş işaretleri olarak gösterilen bir yapılandırılmış belge etiketini temsil eder.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
