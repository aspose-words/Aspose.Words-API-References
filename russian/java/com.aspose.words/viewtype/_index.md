---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words для Java"
description: "Возможные значения режима просмотра в Microsoft Word для Java."
type: docs
weight: 715
url: /ru/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Возможные значения режима просмотра в Microsoft Word.

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
| [NONE](#NONE) | Документ будет отображён в представлении по умолчанию приложения. |
| [NORMAL](#NORMAL) | Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами. |
| [OUTLINE](#OUTLINE) | Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | Документ будет открыт в представлении, показывающем, как он будет печататься. |
| [READING](#READING) | Документ будет отображён в представлении по умолчанию приложения. |
| [WEB](#WEB) | Документ будет отображён в представлении, имитирующем способ отображения этого документа на веб-странице. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Документ будет отображён в представлении по умолчанию приложения.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


Документ будет открыт в представлении, показывающем, как он будет печататься.

### READING {#READING}
```
public static int READING
```


Документ будет отображён в представлении по умолчанию приложения.

### WEB {#WEB}
```
public static int WEB
```


Документ будет отображён в представлении, имитирующем способ отображения этого документа на веб-странице.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
