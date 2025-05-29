---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words для .NET
description: Легко управляйте форматами файлов с помощью Aspose.Words.FileFormatUtil. Легко определяйте форматы и конвертируйте расширения для повышения производительности.
type: docs
weight: 3230
url: /ru/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Предоставляет служебные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в/из перечислений форматов файлов.

Чтобы узнать больше, посетите[Определить формат файла и проверить совместимость формата](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) документальная статья.

```csharp
public static class FileFormatUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Преобразует тип содержимого IANA в перечислимое значение формата загрузки. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Преобразует тип содержимого IANA в формат сохранения перечислимого значения. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Обнаруживает и возвращает информацию о формате документа, хранящегося в потоке. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Обнаруживает и возвращает информацию о формате документа, хранящегося в файле на диске. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Преобразует расширение имени файла в[`SaveFormat`](../saveformat/) значение. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Преобразует перечислимое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение — это строка в нижнем регистре с точкой в начале. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Преобразует значение формата загрузки в расширение файла. Возвращаемое расширение — это строка в нижнем регистре с точкой в начале. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Преобразует[`LoadFormat`](../loadformat/) значение для[`SaveFormat`](../saveformat/) значение, если возможно. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Преобразует значение формата сохранения перечисления в расширение файла. Возвращаемое расширение — это строка в нижнем регистре с точкой в начале. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Преобразует[`SaveFormat`](../saveformat/) значение для[`LoadFormat`](../loadformat/) значение, если возможно. |

## Примеры

Показывает, как определить кодировку в HTML-файле.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Свойство Encoding используется только при создании объекта FileFormatInfo для HTML-документа.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
