---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words Java için"
description: "Java'da filigran tipini belirtir."
type: docs
weight: 723
url: /tr/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Filigran türünü belirtir.

 **Examples:** 

Metin filigranı oluşturmayı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [IMAGE](#IMAGE) | Görselin filigran olarak kullanılacağını gösterir. |
| [NONE](#NONE) | Filigranın ayarlanmadığını gösterir. |
| [TEXT](#TEXT) | Metnin filigran olarak kullanılacağını gösterir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Görselin filigran olarak kullanılacağını gösterir.

Böyle bir filigran, görüntülü bir şekle karşılık gelir.

### NONE {#NONE}
```
public static int NONE
```


Filigranın ayarlanmadığını gösterir.

### TEXT {#TEXT}
```
public static int TEXT
```


Metnin filigran olarak kullanılacağını gösterir.

Böyle bir filigran, bir WordArt nesnesine karşılık gelir.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
