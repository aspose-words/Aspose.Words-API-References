---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words для .NET
description: Легко обновите миниатюру вашего документа с помощью наших настраиваемых опций. Улучшите визуальные эффекты и презентацию документа сегодня!
type: docs
weight: 840
url: /ru/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Обновления[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа согласно указанным параметрам.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Параметры генерации для использования. |

## Примечания

[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) позволяет указать источник миниатюры, размер и другие параметры. Если попытка создания миниатюры не удалась, не изменяет ее.

## Примеры

Показывает, как обновить миниатюру документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Существует два способа установки миниатюры изображения при сохранении документа в формате .epub.
// 1 — Использовать первую страницу документа:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 — Использовать первое изображение, найденное в документе:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Смотрите также

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Обновления[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа с использованием параметров по умолчанию.

```csharp
public void UpdateThumbnail()
```

## Примеры

Показывает, как обновить миниатюру документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Существует два способа установки миниатюры изображения при сохранении документа в формате .epub.
// 1 — Использовать первую страницу документа:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 — Использовать первое изображение, найденное в документе:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
