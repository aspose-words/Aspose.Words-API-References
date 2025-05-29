---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSize объекта ImageSaveOptions, чтобы легко управлять и настраивать размеры изображения в пикселях для достижения оптимальных результатов.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Получает или задает размер сгенерированного изображения в пикселях.

```csharp
public Size ImageSize { get; set; }
```

## Примечания

Это свойство действует только при сохранении в растровых форматах изображений.

Значение по умолчанию — (0 x 0), что означает, что размер сгенерированного изображения будет рассчитан в соответствии с размером изображения в точках, указанным разрешением и масштабом.

## Примеры

Показывает, как преобразовать каждую страницу документа в отдельное изображение TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Установите свойство "PageSet" на номер первой страницы из
    // с которого начать рендеринг документа.
    options.PageSet = new PageSet(i);
    // Экспортировать страницу с разрешением 2325x5325 пикселей и 600 точек на дюйм.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
