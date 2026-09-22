---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words لـ Java"
description: "يحدد تخطيط العلامة المائية بالنسبة إلى مركز العلامة المائية في جافا."
type: docs
weight: 722
url: /ar/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

يحدد تخطيط العلامة المائية بالنسبة إلى مركز العلامة المائية.

 **Examples:** 

يوضح كيفية إنشاء علامة مائية نصية.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [DIAGONAL](#DIAGONAL) | تخطيط العلامة المائية القطري. |
| [HORIZONTAL](#HORIZONTAL) | تخطيط العلامة المائية الأفقي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


تخطيط العلامة المائية القطري. يتوافق مع دوران قدره 315 درجة.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


تخطيط العلامة المائية الأفقي. يتوافق مع دوران قدره 0 درجة.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
