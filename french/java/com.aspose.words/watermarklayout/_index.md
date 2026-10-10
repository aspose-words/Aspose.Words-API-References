---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words pour Java"
description: "Définit la disposition du filigrane par rapport au centre du filigrane en Java."
type: docs
weight: 722
url: /fr/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Définit la disposition du filigrane par rapport au centre du filigrane.

 **Examples:** 

Montre comment créer un filigrane texte.

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
## Champs

| Champ | Description |
| --- | --- |
| [DIAGONAL](#DIAGONAL) | Disposition du filigrane en diagonale. |
| [HORIZONTAL](#HORIZONTAL) | Disposition du filigrane horizontale. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Disposition du filigrane en diagonale. Correspond à une rotation de 315 degrés.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Disposition du filigrane horizontale. Correspond à une rotation de 0 degré.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
