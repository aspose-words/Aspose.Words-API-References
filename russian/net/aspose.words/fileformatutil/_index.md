---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words для .NET
description: Aspose.Words.FileFormatUtil сорт. Предоставляет служебные методы для работы с форматами файлов такие как определение формата файла или преобразование расширений файлов в перечисления форматов файлов или из них на С#.
type: docs
weight: 2820
url: /ru/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Предоставляет служебные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в перечисления форматов файлов или из них.

Чтобы узнать больше, посетите[Определить формат файла и проверить совместимость форматов](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) статья документации.

```csharp
public static class FileFormatUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Преобразует тип контента IANA в перечисляемое значение формата загрузки. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Преобразует тип контента IANA в перечислимое значение формата сохранения. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Обнаруживает и возвращает информацию о формате документа, хранящегося в потоке. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Обнаруживает и возвращает информацию о формате документа, хранящегося в дисковом файле. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Преобразует расширение имени файла в[`SaveFormat`](../saveformat/) значение. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Преобразует перечислимое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение представляет собой строку в нижнем регистре с начальной точкой. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Преобразует перечисляемое значение формата загрузки в расширение файла. Возвращаемое расширение представляет собой строку в нижнем регистре с начальной точкой. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Преобразует[`LoadFormat`](../loadformat/) ценность для[`SaveFormat`](../saveformat/) значение, если возможно. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Преобразует перечисляемое значение формата сохранения в расширение файла. Возвращаемое расширение представляет собой строку в нижнем регистре с начальной точкой. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Преобразует[`SaveFormat`](../saveformat/) ценность для[`LoadFormat`](../loadformat/) значение, если возможно. |

## Примеры

Показывает, как определить кодировку в html-файле.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Свойство Encoding используется только тогда, когда мы создаем объект FileFormatInfo для html-документа.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
