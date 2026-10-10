---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words für Java"
description: "Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens in Java."
type: docs
weight: 722
url: /de/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens.

 **Examples:** 

Zeigt, wie man ein Textwasserzeichen erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DIAGONAL](#DIAGONAL) | Diagonales Wasserzeichen-Layout. |
| [HORIZONTAL](#HORIZONTAL) | Horizontales Wasserzeichen-Layout. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Diagonales Wasserzeichen-Layout. Entspricht einer Drehung von 315 Grad.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontales Wasserzeichen-Layout. Entspricht einer Drehung von 0 Grad.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
