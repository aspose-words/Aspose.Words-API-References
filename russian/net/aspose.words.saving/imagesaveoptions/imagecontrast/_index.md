---
title: ImageSaveOptions.ImageContrast
linktitle: ImageContrast
articleTitle: ImageContrast
second_title: Aspose.Words для .NET
description: Отрегулируйте свойство ImageContrast в ImageSaveOptions, чтобы улучшить четкость и глубину изображений. Оптимизируйте визуальные эффекты без усилий!
type: docs
weight: 60
url: /ru/net/aspose.words.saving/imagesaveoptions/imagecontrast/
---
## ImageSaveOptions.ImageContrast property

Получает или задает контрастность для созданных изображений.

```csharp
public float ImageContrast { get; set; }
```

## Примечания

Это свойство действует только при сохранении в растровых форматах изображений.

Значение по умолчанию 0,5. Значение должно быть в диапазоне от 0 до 1.

## Примеры

Показывает, как редактировать изображение, пока Aspose.Words преобразует в него документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// редактируем изображение, пока операция сохранения его рендерит.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Мы можем настроить эти свойства, чтобы изменить яркость и контрастность изображения.
    // Оба имеют шкалу от 0 до 1 и по умолчанию равны 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // С помощью этих свойств мы можем настроить горизонтальное и вертикальное разрешение.
    // Это повлияет на размеры изображения.
    // Значение по умолчанию для этих свойств — 96,0 для разрешения 96 точек на дюйм.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0, для масштабирования 100%.
    // Мы можем использовать это свойство, чтобы свести на нет любые изменения размеров изображения, которые могут возникнуть при изменении разрешения.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
