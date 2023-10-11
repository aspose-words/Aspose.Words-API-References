---
title: ImageSaveOptions.ImageSize
second_title: Справочник по API Aspose.Words для .NET
description: ImageSaveOptions свойство. Получает или задает размер созданного изображения в пикселях.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Получает или задает размер созданного изображения в пикселях.

```csharp
public Size ImageSize { get; set; }
```

### Примечания

Это свойство действует только при сохранении в форматах растровых изображений.

Значение по умолчанию — (0 x 0), что означает, что размер сгенерированного изображения будет рассчитываться в соответствии с размером изображения в точках, указанным разрешением и масштабом.

### Примеры

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

// Создаем объект ImageSaveOptions, который мы можем передать методу Save документа.
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Устанавливаем для свойства "PageSet" номер первой страницы из
    // с чего начать рендеринг документа.
    options.PageSet = new PageSet(i);
    // Экспортируем страницу с разрешением 2325x5325 пикселей и разрешением 600 точек на дюйм.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../imagesaveoptions/)
* сборка [Aspose.Words](../../../)


