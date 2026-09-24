---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words Java için"
description: "Java'da filigranın merkeze göre düzenini tanımlar."
type: docs
weight: 722
url: /tr/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Filigranın merkeze göre yerleşimini tanımlar.

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
| [DIAGONAL](#DIAGONAL) | Diyagonal filigran düzeni. |
| [HORIZONTAL](#HORIZONTAL) | Yatay filigran düzeni. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Diyagonal filigran düzeni. 315 derece dönüşe karşılık gelir.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Yatay filigran düzeni. 0 derece dönüşe karşılık gelir.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
