---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words для Java"
description: "Указывает, как документ выводится на печать в Java."
type: docs
weight: 473
url: /ru/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Указывает, как документ печатается.

 **Examples:** 

Показывает, как настроить документ, который можно распечатать в виде книжного сгиба.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Указывает, печатать ли документ в виде книжного сгиба. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Указывает, печатать ли документ в виде обратного книжного сгиба. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Меняет местами левый и правый поля на соседних страницах. |
| [NORMAL](#NORMAL) | Обычная печать, без указания нескольких страниц. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Печатает две страницы на лист. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Указывает, печатать ли документ в виде книжного сгиба.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Указывает, печатать ли документ в виде обратного книжного сгиба.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Меняет местами левый и правый поля на соседних страницах.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Обычная печать, без указания нескольких страниц.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Печатает две страницы на лист.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int multiplePagesType) {#toString-int}
```
public static String toString(int multiplePagesType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
