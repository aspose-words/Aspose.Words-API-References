---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words für Java"
description: "Definiert das Trennzeichenzeichen, das zwischen Kapitel‑ und Seitennummer in Java erscheint."
type: docs
weight: 65
url: /de/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Definiert das Trennzeichen, das zwischen Kapitel- und Seitenzahl erscheint.

 **Examples:** 

Zeigt, wie man mit Seitenkapiteln arbeitet.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [COLON](#COLON) | Ein Doppelpunkt. |
| [EM_DASH](#EM-DASH) | Ein betonter Bindestrich. |
| [EN_DASH](#EN-DASH) | Ein Standard‑Bindestrich. |
| [HYPHEN](#HYPHEN) | Ein Doppelpunkt. |
| [PERIOD](#PERIOD) | Ein Punkt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


Ein Doppelpunkt.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Ein betonter Bindestrich.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Ein Standard‑Bindestrich.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


Ein Doppelpunkt.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


Ein Punkt.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
