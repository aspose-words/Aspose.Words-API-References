---
title: WatermarkType
linktitle: WatermarkType
second_title: Aspose.Words for Java
description: Specifies the watermark type in Java.
type: docs
weight: 633
url: /java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Specifies the watermark type.

 **Examples:** 

Shows how to create a text watermark.

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
## Fields

| Field | Description |
| --- | --- |
| [IMAGE](#IMAGE) | Indicates that the image will be used as a watermark. |
| [NONE](#NONE) | Indicates watermark is no set. |
| [TEXT](#TEXT) | Indicates that the text will be used as a watermark. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indicates that the image will be used as a watermark.

Such a watermark corresponds to a shape with image.

### NONE {#NONE}
```
public static int NONE
```


Indicates watermark is no set.

### TEXT {#TEXT}
```
public static int TEXT
```


Indicates that the text will be used as a watermark.

Such a watermark corresponds to a WordArt object.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
