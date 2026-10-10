---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как объекты InkML чернил отображаются в фиксированные форматы страниц в Java."
type: docs
weight: 399
url: /ru/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Указывает, как объекты чернил (InkML) рендерятся в фиксированные форматы страниц.

 **Examples:** 

Показывает, как отрисовывать объект Ink.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FALLBACK](#FALLBACK) | Если для объекта ink (InkML) доступна резервная форма, Aspose.Words отрисовывает резервную форму вместо InkML. |
| [INK_ML](#INK-ML) | Aspose.Words игнорирует резервную форму объекта ink (InkML) и отрисовывает сам InkML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Если для объекта ink (InkML) доступна резервная форма, Aspose.Words отрисовывает резервную форму вместо InkML.

 **Remarks:** 

Обратите внимание, что после сохранения документа в фиксированный формат страницы с режимом резервного рендеринга объекты InkML в модели документа AW навсегда заменяются их резервными аналогами. В результате повторное сохранение того же документа всегда будет использовать резервные формы, даже если [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) установлен в [INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words игнорирует резервную форму объекта ink (InkML) и отрисовывает сам InkML. Это режим по умолчанию.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imlRenderingMode) {#toString-int}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
