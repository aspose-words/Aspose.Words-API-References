---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de filigrane en Java."
type: docs
weight: 723
url: /fr/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Spécifie le type de filigrane.

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
| [IMAGE](#IMAGE) | Indique que l’image sera utilisée comme filigrane. |
| [NONE](#NONE) | Indique que le filigrane n’est pas défini. |
| [TEXT](#TEXT) | Indique que le texte sera utilisé comme filigrane. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indique que l’image sera utilisée comme filigrane.

Un tel filigrane correspond à une forme avec image.

### NONE {#NONE}
```
public static int NONE
```


Indique que le filigrane n’est pas défini.

### TEXT {#TEXT}
```
public static int TEXT
```


Indique que le texte sera utilisé comme filigrane.

Un tel filigrane correspond à un objet WordArt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
