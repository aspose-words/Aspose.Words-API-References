---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words для .NET
description: Узнайте, как опция GenerateFromFirstPage создает миниатюры из первой страницы или изображения документа, легко улучшая визуальный контент.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Указывает, следует ли создавать миниатюру с первой страницы документа или с первого изображения.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` , что означает, что миниатюра будет создана с первой страницы документа. Если значение равно`ЛОЖЬ` и в документе нет изображения, миниатюра будет создана с первой страницы документа.

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

* class [ThumbnailGeneratingOptions](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
