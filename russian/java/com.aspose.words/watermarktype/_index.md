---
title: "WatermarkType"
linktitle: "WatermarkType"
second_title: "Aspose.Words для Java"
description: "Указывает тип водяного знака в Java."
type: docs
weight: 723
url: /ru/java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Указывает тип водяного знака.

 **Examples:** 

Показывает, как создать текстовый водяной знак.

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
## Поля

| Поле | Описание |
| --- | --- |
| [IMAGE](#IMAGE) | Указывает, что изображение будет использоваться как водяной знак. |
| [NONE](#NONE) | Указывает, что водяной знак не установлен. |
| [TEXT](#TEXT) | Указывает, что текст будет использоваться как водяной знак. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkType)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Указывает, что изображение будет использоваться как водяной знак.

Такой водяной знак соответствует фигуре с изображением.

### NONE {#NONE}
```
public static int NONE
```


Указывает, что водяной знак не установлен.

### TEXT {#TEXT}
```
public static int TEXT
```


Указывает, что текст будет использоваться как водяной знак.

Такой водяной знак соответствует объекту WordArt.

### length {#length}
```
public static int length
```


### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
