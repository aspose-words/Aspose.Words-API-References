---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de marca de agua en Java."
type: docs
weight: 723
url: /es/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Especifica el tipo de marca de agua.

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
| [IMAGE](#IMAGE) | Indica que la imagen se usará como marca de agua. |
| [NONE](#NONE) | Indica que la marca de agua no está establecida. |
| [TEXT](#TEXT) | Indica que el texto se usará como marca de agua. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indica que la imagen se usará como marca de agua.

Una marca de agua de este tipo corresponde a una forma con imagen.

### NONE {#NONE}
```
public static int NONE
```


Indica que la marca de agua no está establecida.

### TEXT {#TEXT}
```
public static int TEXT
```


Indica que el texto se usará como marca de agua.

Una marca de agua de este tipo corresponde a un objeto WordArt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int watermarkType) {#toString-int}
```
public static String toString(int watermarkType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
