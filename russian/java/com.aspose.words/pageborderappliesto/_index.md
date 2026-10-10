---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words для Java"
description: "Указывает, на каких страницах печатается граница страницы в Java."
type: docs
weight: 510
url: /ru/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Указывает, на каких страницах печатается граница страницы.

 **Examples:** 

Показывает, как создать широкую синюю полосу‑границу в верхней части первой страницы.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | Граница страницы отображается на всех страницах раздела. |
| [FIRST_PAGE](#FIRST-PAGE) | Граница страницы отображается только на первой странице раздела. |
| [OTHER_PAGES](#OTHER-PAGES) | Граница страницы отображается на всех страницах, кроме первой страницы раздела. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


Граница страницы отображается на всех страницах раздела.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


Граница страницы отображается только на первой странице раздела.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


Граница страницы отображается на всех страницах, кроме первой страницы раздела.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderAppliesTo) {#toString-int}
```
public static String toString(int pageBorderAppliesTo)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
