---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как эффекты DrawingML рендерятся в фиксированные форматы страниц в Java."
type: docs
weight: 157
url: /ru/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

Указывает, как эффекты DrawingML отображаются в фиксированных форматах страниц.

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
## Поля

| Поле | Описание |
| --- | --- |
| [FINE](#FINE) | Эффекты DrawingML рендерятся в точном режиме, который включает расширенную обработку. |
| [NONE](#NONE) | Эффекты DrawingML не рендерятся. |
| [SIMPLIFIED](#SIMPLIFIED) | Рендеринг эффектов DrawingML упрощён. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


Эффекты DrawingML рендерятся в точном режиме, который включает расширенную обработку. В этом режиме рендеринг эффектов дает лучшие результаты, но требует больших затрат производительности по сравнению с режимом [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

### NONE {#NONE}
```
public static int NONE
```


Эффекты DrawingML не рендерятся.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


Рендеринг эффектов DrawingML упрощён.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlEffectsRenderingMode) {#toString-int}
```
public static String toString(int dmlEffectsRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
