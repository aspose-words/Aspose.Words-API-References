---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words для .NET
description: Легко конвертируйте ваши документы с помощью метода Convert нашего конвертера. Преобразуйте входные файлы в нужные форматы с легкостью и точностью.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и их расширения.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| outputFile | String | Имя выходного файла. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как преобразовать документы с помощью одной строки кода.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Смотрите также

* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и формат конечного документа.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| outputFile | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как преобразовать документы с помощью одной строки кода.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и параметры сохранения.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| outputFile | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как преобразовать документы с помощью одной строки кода.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Преобразует заданный входной документ в выходной документ, используя указанные имена входных и выходных файлов и параметры загрузки/сохранения.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| loadOptions | LoadOptions | Параметры загрузки входного документа. |
| outputFile | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как преобразовать документы с помощью одной строки кода.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как конвертировать документы с помощью одной строки кода (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входные потоки. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как конвертировать документы с помощью одной строки кода (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входные потоки. |
| loadOptions | LoadOptions | Параметры загрузки входного документа. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как конвертировать документы с помощью одной строки кода (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
