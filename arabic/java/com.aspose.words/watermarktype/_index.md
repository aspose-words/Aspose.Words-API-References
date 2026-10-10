---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع العلامة المائية في Java."
type: docs
weight: 723
url: /ar/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

يحدد نوع العلامة المائية.

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
| [IMAGE](#IMAGE) | يشير إلى أن الصورة ستُستخدم كعلامة مائية. |
| [NONE](#NONE) | يشير إلى أن العلامة المائية غير مُحددة. |
| [TEXT](#TEXT) | يشير إلى أن النص سيُستخدم كعلامة مائية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


يشير إلى أن الصورة ستُستخدم كعلامة مائية.

تطابق هذه العلامة المائية شكلًا يحتوي على صورة.

### NONE {#NONE}
```
public static int NONE
```


يشير إلى أن العلامة المائية غير مُحددة.

### TEXT {#TEXT}
```
public static int TEXT
```


يشير إلى أن النص سيُستخدم كعلامة مائية.

تطابق هذه العلامة المائية كائن WordArt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
