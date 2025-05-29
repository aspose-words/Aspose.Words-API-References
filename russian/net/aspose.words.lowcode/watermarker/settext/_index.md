---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью нашего метода Watermarker SetText. Легко добавляйте настраиваемые текстовые водяные знаки для улучшения брендинга и профессионализма.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

Добавляет текстовый водяной знак в документ.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| watermarkText | String | Текст, отображаемый как водяной знак. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить текст водяного знака в документ.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Смотрите также

* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

Добавляет текстовый водяной знак в документ с параметрами.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить текст водяного знака в документ.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Смотрите также

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как вставить текст водяного знака в документ.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

Добавляет текстовый водяной знак в документ из потоков с параметрами.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как вставить текст водяного знака в документ из потока.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

Добавляет текстовый водяной знак в документ из потоков с параметрами.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| watermarkText | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
