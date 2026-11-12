---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words для Java"
description: "Определяет символ‑разделитель, который появляется между номером главы и номером страницы в Java."
type: docs
weight: 65
url: /ru/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Определяет символ-разделитель, который появляется между номером главы и номером страницы.

 **Examples:** 

Показывает, как работать с главами страниц.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [COLON](#COLON) | Двоеточие. |
| [EM_DASH](#EM-DASH) | Выделенное тире. |
| [EN_DASH](#EN-DASH) | Стандартное тире. |
| [HYPHEN](#HYPHEN) | Двоеточие. |
| [PERIOD](#PERIOD) | Точка. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


Двоеточие.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


Выделенное тире.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


Стандартное тире.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


Двоеточие.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


Точка.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
