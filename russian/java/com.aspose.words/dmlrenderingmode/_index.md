---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как формы DrawingML отображаются в фиксированные форматы страниц в Java."
type: docs
weight: 158
url: /ru/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Указывает, как формы DrawingML отображаются в фиксированных форматах страниц.

 **Examples:** 

Показывает, как настроить качество рендеринга эффектов DrawingML в документе при сохранении его в PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

Показывает, как отрисовывать резервные формы при сохранении в PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words игнорирует резервную форму DrawingML и отрисовывает сам DrawingML. |
| [FALLBACK](#FALLBACK) | Если для DrawingML доступна резервная форма, Aspose.Words отрисовывает резервную форму вместо DrawingML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words игнорирует резервную форму DrawingML и отрисовывает сам DrawingML. Это режим по умолчанию.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Если для DrawingML доступна резервная форма, Aspose.Words отрисовывает резервную форму вместо DrawingML.

 **Remarks:** 

Обратите внимание, что после сохранения документа в фиксированный формат страниц с режимом резервного рендеринга DML, формы DML в модели документа AW постоянно заменяются их резервными аналогами. В результате повторное сохранение того же документа всегда будет использовать резервные формы, даже если [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) установлен в [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlRenderingMode) {#toString-int}
```
public static String toString(int dmlRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
