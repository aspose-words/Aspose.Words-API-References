---
title: "PdfImageColorSpaceExportMode"
linktitle: "PdfImageColorSpaceExportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как будет выбираться цветовое пространство для изображений в PDF‑документе на Java."
type: docs
weight: 536
url: /ru/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Указывает, как будет выбран цветовое пространство для изображений в PDF‑документе.

 **Examples:** 

Показывает, как установить другое цветовое пространство для изображений в документе при экспорте в PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jpeg image:");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertParagraph();
 builder.writeln("Png image:");
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
 // automatically select the color space for images in the document that it converts to PDF.
 // In most cases, the color space will be RGB.
 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
 // to use the CMYK color space for all images in the saved PDF.
 // Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
 pdfSaveOptions.setImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words автоматически выбирает наиболее подходящее цветовое пространство для каждого изображения. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words преобразует RGB‑изображения в цветовое пространство CMYK, используя простую формулу. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words автоматически выбирает наиболее подходящее цветовое пространство для каждого изображения.

 **Remarks:** 

Большинство изображений сохраняются в цветовом пространстве RGB. Также могут использоваться Indexed и Grayscale. Цветовое пространство CMYK никогда не используется.

Для некоторых изображений цветовое пространство может отличаться на разных платформах.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words преобразует RGB‑изображения в цветовое пространство CMYK, используя простую формулу.

 **Remarks:** 

Изображения в цветовом пространстве RGB преобразуются в CMYK по формуле: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). Значения RGB нормализованы — они находятся в диапазоне от 0 до 1.0.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageColorSpaceExportMode) {#toString-int}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
