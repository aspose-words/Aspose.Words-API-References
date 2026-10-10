---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words для Java"
description: "Указывает тип разделителя сносок/конечных сносок в Java."
type: docs
weight: 345
url: /ru/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Указывает тип разделителя сноски/концевой сноски.

 **Examples:** 

Показывает, как удалить разделитель конечных сносок.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Показывает, как управлять форматом разделителя сносок.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Печатается под текстом конечной сноски на странице, когда текст конечной сноски должен продолжаться на следующей странице. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Печатается над текстом конечной сноски на странице, когда текст должен продолжаться с предыдущей страницы. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Разделитель между основным текстом и текстом конечной сноски. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Печатается под текстом сноски на странице, когда текст сноски должен продолжаться на следующей странице. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Печатается над текстом сноски на странице, когда текст должен продолжаться с предыдущей страницы. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Разделитель между основным текстом и текстом сноски. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Печатается под текстом конечной сноски на странице, когда текст конечной сноски должен продолжаться на следующей странице.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Печатается над текстом конечной сноски на странице, когда текст должен продолжаться с предыдущей страницы.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Разделитель между основным текстом и текстом конечной сноски.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Печатается под текстом сноски на странице, когда текст сноски должен продолжаться на следующей странице.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Печатается над текстом сноски на странице, когда текст должен продолжаться с предыдущей страницы.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Разделитель между основным текстом и текстом сноски.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
