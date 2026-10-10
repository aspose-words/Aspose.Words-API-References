---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words per Java"
description: "Definisce il layout della filigrana rispetto al centro della filigrana in Java."
type: docs
weight: 722
url: /it/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Definisce il layout della filigrana rispetto al centro della filigrana.

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
| [DIAGONAL](#DIAGONAL) | Layout della filigrana diagonale. |
| [HORIZONTAL](#HORIZONTAL) | Layout della filigrana orizzontale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Layout della filigrana diagonale. Corrisponde a una rotazione di 315 gradi.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Layout della filigrana orizzontale. Corrisponde a una rotazione di 0 gradi.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
