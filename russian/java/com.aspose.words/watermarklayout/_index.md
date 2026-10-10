---
title: "WatermarkLayout"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words для Java"
description: "Определяет расположение водяного знака относительно его центра в Java."
type: docs
weight: 722
url: /ru/java/com.aspose.words/watermarklayout/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkLayout
```

Определяет расположение водяного знака относительно его центра.

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
| [DIAGONAL](#DIAGONAL) | Диагональное расположение водяного знака. |
| [HORIZONTAL](#HORIZONTAL) | Горизонтальное расположение водяного знака. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String watermarkLayoutName)](#fromName-java.lang.String) |  |
| [getName(int watermarkLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int watermarkLayout)](#toString-int) |  |
### DIAGONAL {#DIAGONAL}
```
public static int DIAGONAL
```


Диагональное расположение водяного знака. Соответствует повороту на 315 градусов.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Горизонтальное расположение водяного знака. Соответствует повороту на 0 градусов.

### length {#length}
```
public static int length
```


### fromName(String watermarkLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkLayoutName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| watermarkLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int watermarkLayout) {#getName-int}
```
public static String getName(int watermarkLayout)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| watermarkLayout | int |  |

**Returns:**
java.lang.String
