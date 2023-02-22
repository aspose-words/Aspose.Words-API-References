---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
second_title: Справочник по API Aspose.Words для .NET
description: ThumbnailGeneratingOptions свойство. Указывает следует ли создавать миниатюру из первой страницы документа или первого изображения.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Указывает, следует ли создавать миниатюру из первой страницы документа или первого изображения.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

### Примечания

По умолчанию`истинный` , что означает, что миниатюра будет создана с первой страницы документа. Если значение равно`ЛОЖЬ` и в документе нет изображения, миниатюра будет сгенерирована с первой страницы документа.

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

* class [ThumbnailGeneratingOptions](../)
* пространство имен [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* сборка [Aspose.Words](../../../)


