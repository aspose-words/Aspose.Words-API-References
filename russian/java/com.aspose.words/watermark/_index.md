---
title: "Водяной знак"
linktitle: "Водяной знак"
second_title: "Aspose.Words для Java"
description: "Представляет класс для работы с водяным знаком документа в Java."
type: docs
weight: 721
url: /ru/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Представляет класс для работы с водяным знаком документа.

Чтобы узнать больше, посетите статью документации [ Working with Watermark ][Working with Watermark].

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


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Методы

| Метод | Описание |
| --- | --- |
| [getType()](#getType) | Получает тип водяного знака. |
| [remove()](#remove) | Удаляет водяной знак. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Добавляет изображение водяного знака в документ. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение водяного знака в документ. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение водяного знака в документ. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение водяного знака в документ. |
| [setText(String text)](#setText-java.lang.String) | Добавляет текстовый водяной знак в документ. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак в документ. |
### getType() {#getType}
```
public int getType()
```


Получает тип водяного знака.

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

**Returns:**
int — тип водяного знака. Возвращаемое значение является одной из констант [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


Удаляет водяной знак.

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

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Добавляет изображение водяного знака в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | java.awt.image.BufferedImage | Изображение, отображаемое как водяной знак. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Добавляет изображение водяного знака в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | java.awt.image.BufferedImage | Изображение, отображаемое как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Добавляет изображение водяного знака в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageStream | java.io.InputStream | Поток, содержащий данные изображения, отображаемого как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Добавляет изображение водяного знака в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | java.lang.String | Путь к файлу изображения, отображаемому как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Добавляет текстовый водяной знак в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Текст, отображаемый как водяной знак. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Текст, отображаемый как водяной знак. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Определяет дополнительные параметры для текста водяного знака. |

