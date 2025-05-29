---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words для .NET
description: Преобразуйте свои документы без усилий с ConvertToImages. Быстро и легко преобразуйте страницы в высококачественные файлы изображений для улучшенного обмена и хранения.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Преобразует страницы указанного входного файла в изображения указанного формата и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| saveFormat | SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в поток изображений.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Преобразует страницы указанного входного файла в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения изображения. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в поток изображений.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Преобразует страницы указанного входного потока в изображения в указанном формате и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| saveFormat | SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в изображение из потока.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Преобразует страницы указанного входного потока в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения изображения. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в изображение из потока.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| loadOptions | LoadOptions | Параметры загрузки входного документа. |
| saveOptions | ImageSaveOptions | Параметры сохранения изображения. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в изображение из потока.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Преобразует страницы указанного документа в изображения указанного формата и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | Document | Входной документ. |
| saveFormat | SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в поток изображений.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Смотрите также

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Преобразует страницы указанного документа в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | Document | Входной документ. |
| saveOptions | ImageSaveOptions | Параметры сохранения изображения. |

### Возвращаемое значение

Возвращает массив потоков изображений. Потоки должны быть удалены конечным пользователем.

## Примеры

Показывает, как преобразовать документ в поток изображений.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
