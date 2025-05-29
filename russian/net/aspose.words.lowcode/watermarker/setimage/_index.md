---
title: Watermarker.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью метода Watermarker SetImage. Легко добавляйте пользовательские водяные знаки для профессионального штриха.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/watermarker/setimage/
---
## SetImage(*string, string, string*) {#setimage_6}

Добавляет водяной знак в документ.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| watermarkImageFileName | String | Изображение, отображаемое как водяной знак. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить изображение водяного знака в документ.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Смотрите также

* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*string, string, string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_7}

Добавляет водяной знак в документ с параметрами.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| watermarkImageFileName | String | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить изображение водяного знака в документ.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Смотрите также

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_4}

Добавляет водяной знак в документ с параметрами и указанным форматом сохранения.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |
| watermarkImageFileName | String | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить изображение водяного знака в документ.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_5}

Добавляет водяной знак в документ с параметрами и указанным форматом сохранения.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |
| watermarkImageFileName | String | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage}

Добавляет водяной знак изображения в документ из потоков с параметрами.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| watermarkImage | Image | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как вставить изображение водяного знака в документ из потока.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"));
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"), new ImageWatermarkOptions() { Scale = 50 });
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_2}

Добавляет водяной знак изображения в документ из потоков с параметрами.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| watermarkImage | Image | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_1}

Добавляет водяной знак изображения в документ из потоков с параметрами.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| watermarkImageStream | Stream | Поток изображения, отображаемый в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_3}

Добавляет водяной знак изображения в документ из потоков с параметрами.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| watermarkImageStream | Stream | Поток изображения, отображаемый в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
