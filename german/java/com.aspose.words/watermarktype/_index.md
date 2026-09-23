---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words für Java"
description: "Gibt den Wasserzeichen-Typ in Java an."
type: docs
weight: 723
url: /de/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Gibt den Wasserzeichentyp an.

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
| [IMAGE](#IMAGE) | Zeigt an, dass das Bild als Wasserzeichen verwendet wird. |
| [NONE](#NONE) | Gibt an, dass das Wasserzeichen nicht gesetzt ist. |
| [TEXT](#TEXT) | Gibt an, dass der Text als Wasserzeichen verwendet wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Zeigt an, dass das Bild als Wasserzeichen verwendet wird.

Ein solches Wasserzeichen entspricht einer Form mit Bild.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass das Wasserzeichen nicht gesetzt ist.

### TEXT {#TEXT}
```
public static int TEXT
```


Gibt an, dass der Text als Wasserzeichen verwendet wird.

Ein solches Wasserzeichen entspricht einem WordArt-Objekt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
