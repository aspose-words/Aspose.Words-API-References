---
title: ImageSaveOptions.GraphicsQualityOptions
second_title: Справочник по API Aspose.Words для .NET
description: ImageSaveOptions свойство. Позволяет указать режим и качество рендеринга дляGraphics объект.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Позволяет указать режим и качество рендеринга дляGraphics объект.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

### Примечания

Используйте это свойство, чтобы переопределить настройки графики, предоставляемые движком Aspose.Words по умолчанию.

Оно вступит в силу только тогда, когда документ сохраняется в формате изображения.

### Примеры

Показывает, как настроить параметры качества рендеринга при преобразовании документов в форматы изображений.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Смотрите также

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../imagesaveoptions/)
* сборка [Aspose.Words](../../../)


