---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words для Java"
description: "Определяет тип верхнего или нижнего колонтитула, найденного в файле Word на Java."
type: docs
weight: 372
url: /ru/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Определяет тип верхнего или нижнего колонтитула, найденного в файле Word. Это верхний/нижний колонтитул конкретного раздела. Не переименовывайте, так как значение перечисления используется как индекс в plcfhdd.

 **Examples:** 

Показывает, как создавать колонтитулы в документе с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Нижний колонтитул для чётных страниц. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Нижний колонтитул для первой страницы раздела. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Основной нижний колонтитул, также используется для нечётных страниц. |
| [HEADER_EVEN](#HEADER-EVEN) | Верхний колонтитул для чётных страниц. |
| [HEADER_FIRST](#HEADER-FIRST) | Верхний колонтитул для первой страницы раздела. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Основной верхний колонтитул, также используется для нечётных страниц. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Нижний колонтитул для чётных страниц.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Нижний колонтитул для первой страницы раздела.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Основной нижний колонтитул, также используется для нечётных страниц.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Верхний колонтитул для чётных страниц.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Верхний колонтитул для первой страницы раздела.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Основной верхний колонтитул, также используется для нечётных страниц.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterType) {#toString-int}
```
public static String toString(int headerFooterType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
