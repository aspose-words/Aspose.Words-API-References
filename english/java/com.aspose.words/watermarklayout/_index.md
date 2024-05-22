---
title: WatermarkLayout
linktitle: WatermarkLayout
second_title: Aspose.Words for Java
description: Defines layout of the watermark relative to the watermark center in Java.
type: docs
weight: 658
url: /java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Defines layout of the watermark relative to the watermark center.

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
| [DIAGONAL](#DIAGONAL) | Diagonal watermark layout. |
| [HORIZONTAL](#HORIZONTAL) | Horizontal watermark layout. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Diagonal watermark layout. Corresponds to 315 degrees of rotation.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontal watermark layout. Corresponds to 0 degrees of rotation.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
