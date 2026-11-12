---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как отображаются цвета в Java."
type: docs
weight: 105
url: /ru/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Указывает, как отображаются цвета.

 **Examples:** 

Показывает, как изменить цвет изображения с помощью свойства параметров сохранения.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Отображение с цветами в диапазоне оттенков серого от белого до чёрного. |
| [NORMAL](#NORMAL) | Отображение с неизменёнными цветами. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Отображение с цветами в диапазоне оттенков серого от белого до чёрного.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Отображение с неизменёнными цветами.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorMode) {#toString-int}
```
public static String toString(int colorMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
