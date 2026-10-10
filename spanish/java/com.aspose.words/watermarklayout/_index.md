---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words para Java"
description: "Define el diseño de la marca de agua relativo al centro de la marca de agua en Java."
type: docs
weight: 722
url: /es/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Define la disposición de la marca de agua relativa al centro de la marca de agua.

 **Examples:** 

Muestra cómo crear una marca de agua de texto.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [DIAGONAL](#DIAGONAL) | Diseño de marca de agua diagonal. |
| [HORIZONTAL](#HORIZONTAL) | Diseño de marca de agua horizontal. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Diseño de marca de agua diagonal. Corresponde a una rotación de 315 grados.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Diseño de marca de agua horizontal. Corresponde a una rotación de 0 grados.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int watermarkLayout) {#toString-int}
```
public static String toString(int watermarkLayout)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
