---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di filigrana in Java."
type: docs
weight: 723
url: /it/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Specifica il tipo di filigrana.

 **Examples:** 

Mostra come creare una filigrana di testo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [IMAGE](#IMAGE) | Indica che l'immagine sarà usata come filigrana. |
| [NONE](#NONE) | Indica che la filigrana non è impostata. |
| [TEXT](#TEXT) | Indica che il testo sarà usato come filigrana. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indica che l'immagine sarà usata come filigrana.

Una tale filigrana corrisponde a una forma con immagine.

### NONE {#NONE}
```
public static int NONE
```


Indica che la filigrana non è impostata.

### TEXT {#TEXT}
```
public static int TEXT
```


Indica che il testo sarà usato come filigrana.

Una tale filigrana corrisponde a un oggetto WordArt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
