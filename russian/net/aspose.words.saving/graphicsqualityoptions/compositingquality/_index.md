---
title: GraphicsQualityOptions.CompositingQuality
second_title: Справочник по API Aspose.Words для .NET
description: GraphicsQualityOptions свойство. Получает или задает качество рендеринга составных изображений нарисованных в этом объекте Graphics.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Получает или задает качество рендеринга составных изображений, нарисованных в этом объекте Graphics.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

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

* class [GraphicsQualityOptions](../)
* пространство имен [Aspose.Words.Saving](../../graphicsqualityoptions/)
* сборка [Aspose.Words](../../../)


