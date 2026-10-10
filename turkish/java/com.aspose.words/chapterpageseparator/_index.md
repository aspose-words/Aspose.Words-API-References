---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words Java için"
description: "Java'da bölüm ve sayfa numarası arasında görünen ayırıcı karakteri tanımlar."
type: docs
weight: 65
url: /tr/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Bölüm ve sayfa numarası arasında görünen ayırıcı karakteri tanımlar.

 **Examples:** 

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [COLON](#COLON) | İki nokta. |
| [EM_DASH](#EM-DASH) | Vurgulu bir tire. |
| [EN_DASH](#EN-DASH) | Standart bir tire. |
| [HYPHEN](#HYPHEN) | İki nokta. |
| [PERIOD](#PERIOD) | Nokta. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


İki nokta.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Vurgulu bir tire.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Standart bir tire.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


İki nokta.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


Nokta.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chapterPageSeparator) {#toString-int}
```
public static String toString(int chapterPageSeparator)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
