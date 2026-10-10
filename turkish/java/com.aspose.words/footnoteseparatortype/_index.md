---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words Java için"
description: "Java'da dipnot/sonnot ayırıcı tipini belirtir."
type: docs
weight: 345
url: /tr/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Dipnot/sonnot ayırıcı tipini belirtir.

 **Examples:** 

Sonnot ayırıcıyı nasıl kaldıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Dipnot ayırıcı biçimini nasıl yöneteceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Sonnot metni bir sonraki sayfada devam etmesi gerektiğinde, sayfada sonnot metninin altında yazdırılır. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Metin önceki sayfadan devam etmesi gerektiğinde, sayfada sonnot metninin üstünde yazdırılır. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Ana metin ile sonnot metni arasındaki ayırıcı. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Dipnot metni bir sonraki sayfada devam etmesi gerektiğinde, sayfada dipnot metninin altında yazdırılır. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Metin önceki sayfadan devam etmesi gerektiğinde, sayfada dipnot metninin üstünde yazdırılır. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Ana metin ile dipnot metni arasındaki ayırıcı. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Sonnot metni bir sonraki sayfada devam etmesi gerektiğinde, sayfada sonnot metninin altında yazdırılır.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Metin önceki sayfadan devam etmesi gerektiğinde, sayfada sonnot metninin üstünde yazdırılır.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Ana metin ile sonnot metni arasındaki ayırıcı.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Dipnot metni bir sonraki sayfada devam etmesi gerektiğinde, sayfada dipnot metninin altında yazdırılır.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Metin önceki sayfadan devam etmesi gerektiğinde, sayfada dipnot metninin üstünde yazdırılır.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Ana metin ile dipnot metni arasındaki ayırıcı.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
