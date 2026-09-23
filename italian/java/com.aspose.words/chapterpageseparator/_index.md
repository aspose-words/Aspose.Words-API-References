---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words per Java"
description: "Definisce il carattere separatore che appare tra il capitolo e il numero di pagina in Java."
type: docs
weight: 65
url: /it/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Definisce il carattere separatore che appare tra il capitolo e il numero di pagina.

 **Examples:** 

Mostra come lavorare con i capitoli di pagina.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [COLON](#COLON) | Due punti. |
| [EM_DASH](#EM-DASH) | Un trattino enfatizzato. |
| [EN_DASH](#EN-DASH) | Un trattino standard. |
| [HYPHEN](#HYPHEN) | Due punti. |
| [PERIOD](#PERIOD) | Un punto. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


Due punti.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Un trattino enfatizzato.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Un trattino standard.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


Due punti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
