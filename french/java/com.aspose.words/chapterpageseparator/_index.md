---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words pour Java"
description: "Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page en Java."
type: docs
weight: 65
url: /fr/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page.

 **Examples:** 

Montre comment travailler avec les chapitres de page.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [COLON](#COLON) | Deux points. |
| [EM_DASH](#EM-DASH) | Un tiret emphatique. |
| [EN_DASH](#EN-DASH) | Un tiret standard. |
| [HYPHEN](#HYPHEN) | Deux points. |
| [PERIOD](#PERIOD) | Un point. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


Deux points.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Un tiret emphatique.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Un tiret standard.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


Deux points.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


Un point.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
