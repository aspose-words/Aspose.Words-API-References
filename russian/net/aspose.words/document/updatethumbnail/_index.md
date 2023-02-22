---
title: Document.UpdateThumbnail
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. ОбновленияThumbnail документа по заданным параметрам.
type: docs
weight: 760
url: /ru/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

Обновления[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа по заданным параметрам.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Используемые параметры генерации. |

### Примечания

[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) позволяет указать источник миниатюры, размер и другие параметры. Если попытка создать миниатюру не удалась, не изменяет ее.

### Примеры

Показывает, как обновить миниатюру документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Существует два способа установки миниатюры при сохранении документа в формате .epub.
// 1 - Использовать первую страницу документа:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Использовать первое изображение, найденное в документе:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Смотрите также

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Обновления[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа с параметрами по умолчанию.

```csharp
public void UpdateThumbnail()
```

### Примеры

Показывает, как обновить миниатюру документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Существует два способа установки миниатюры при сохранении документа в формате .epub.
// 1 - Использовать первую страницу документа:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Использовать первое изображение, найденное в документе:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


