---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words для .NET
description: Оптимизируйте свои изображения с помощью ImageSaveOptions! Управляйте горизонтальным и вертикальным разрешением в DPI для потрясающего качества и четкости. Улучшите свои визуальные эффекты сегодня!
type: docs
weight: 130
url: /ru/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Устанавливает горизонтальное и вертикальное разрешение для создаваемых изображений в точках на дюйм.

```csharp
public float Resolution { set; }
```

## Примечания

Это свойство действует только при сохранении в растровых форматах изображений.

## Примеры

Показывает, как указать разрешение при преобразовании документа в PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Установите свойство «Разрешение» на «72», чтобы отобразить документ с разрешением 72 точки на дюйм.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Установите свойство «Разрешение» на «300», чтобы отобразить документ с разрешением 300 точек на дюйм.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
