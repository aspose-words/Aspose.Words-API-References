---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words para Java"
description: "Define el carácter separador que aparece entre el número de capítulo y de página en Java."
type: docs
weight: 65
url: /es/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Define el carácter separador que aparece entre el número de capítulo y el de página.

 **Examples:** 

Muestra cómo trabajar con capítulos de página.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [COLON](#COLON) | Dos puntos. |
| [EM_DASH](#EM-DASH) | Un guion enfatizado. |
| [EN_DASH](#EN-DASH) | Un guion estándar. |
| [HYPHEN](#HYPHEN) | Dos puntos. |
| [PERIOD](#PERIOD) | Un punto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


Dos puntos.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Un guion enfatizado.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Un guion estándar.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


Dos puntos.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


Un punto.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
