---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words для Java"
description: "Возможные значения того, насколько большой или маленький документ отображается на экране в Microsoft Word на Java."
type: docs
weight: 751
url: /ru/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Возможные значения того, насколько большой или маленький документ отображается на экране в Microsoft Word.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CUSTOM](#CUSTOM) | Процент масштабирования задаётся явно. |
| [FULL_PAGE](#FULL-PAGE) | Процент масштабирования автоматически пересчитывается, чтобы поместить одну полную страницу. |
| [NONE](#NONE) | Указывает использовать явный процент масштабирования. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Процент масштабирования автоматически пересчитывается, чтобы соответствовать ширине страницы. |
| [TEXT_FIT](#TEXT-FIT) | Процент масштабирования автоматически пересчитывается, чтобы соответствовать тексту. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Процент масштабирования задаётся явно. Он не пересчитывается автоматически при изменении размера элемента управления.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Процент масштабирования автоматически пересчитывается, чтобы поместить одну полную страницу.

### NONE {#NONE}
```
public static int NONE
```


Указывает использовать явный процент масштабирования. То же, что и [CUSTOM](../../com.aspose.words/zoomtype/\\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Процент масштабирования автоматически пересчитывается, чтобы соответствовать ширине страницы.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Процент масштабирования автоматически пересчитывается, чтобы соответствовать тексту.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
