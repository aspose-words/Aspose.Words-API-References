---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words для .NET
description: Улучшите свои изображения с помощью нашего метода Watermarker Set, добавив настраиваемые текстовые водяные знаки для придания им профессионального вида и безупречного результата.
type: docs
weight: 40
url: /ru/net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

Добавляет текстовый водяной знак в документ с параметрами. Преобразует вывод в изображения.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примеры

Показывает, как вставить текст водяного знака в документ и сохранить результат в виде изображения.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

Добавляет текстовый водяной знак в документ с параметрами. Преобразует вывод в изображения.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примеры

Показывает, как вставить текст водяного знака в документ из потока и сохранить результат в виде изображения.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

Добавляет водяной знак изображения в документ с параметрами. Преобразует вывод в изображения.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| watermarkImageBytes | Byte[] | Байты изображения, отображаемые в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примеры

Показывает, как вставить изображение водяного знака в документ и сохранить результат в виде изображений.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

Добавляет водяной знак изображения в документ с параметрами. Преобразует вывод в изображения.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| watermarkImageStream | Stream | Поток изображения, отображаемый в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примеры

Показывает, как вставить изображение водяного знака в документ из потока и сохранить результат в виде изображений.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
