---
title: FileFormatUtil.ContentTypeToLoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatUtil метод. Преобразует тип контента IANA в перечислимое значение формата загрузки.
type: docs
weight: 10
url: /ru/net/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil.ContentTypeToLoadFormat method

Преобразует тип контента IANA в перечислимое значение формата загрузки.

```csharp
public static LoadFormat ContentTypeToLoadFormat(string contentType)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выбрасывает, когда не может преобразовать. |

### Примеры

Показывает, как найти соответствующий формат загрузки/сохранения Aspose из каждой строки типа мультимедиа.

```csharp
// Методы ContentTypeToSaveFormat/ContentTypeToLoadFormat принимают только официальные имена типов мультимедиа IANA, также известные как типы MIME. 
// Здесь перечислены все допустимые типы мультимедиа: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Попытка связать SaveFormat с частичной строкой типа мультимедиа не сработает.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Если Aspose.Words не имеет соответствующего формата сохранения/загрузки для типа контента, также будет выдано исключение.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Файлы перечисленных ниже типов можно сохранять, но нельзя загружать с помощью Aspose.Words.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// Для типов файлов, которые можно сохранять и загружать, мы можем сопоставить тип носителя как с форматом загрузки, так и с форматом сохранения.
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### Смотрите также

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
* сборка [Aspose.Words](../../../)


