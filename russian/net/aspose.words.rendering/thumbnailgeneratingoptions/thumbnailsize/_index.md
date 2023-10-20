---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
articleTitle: ThumbnailSize
second_title: Aspose.Words для .NET
description: ThumbnailGeneratingOptions ThumbnailSize свойство. Размер созданного эскиза в пикселях. Значение по умолчанию 600x900 на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Размер созданного эскиза в пикселях. Значение по умолчанию: 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

## Примеры

Показывает, как обновить миниатюру документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Существует два способа установки миниатюры изображения при сохранении документа в формате .epub.
// 1 - Использовать первую страницу документа:
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

* class [ThumbnailGeneratingOptions](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
