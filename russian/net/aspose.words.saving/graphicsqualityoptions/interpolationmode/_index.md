---
title: GraphicsQualityOptions.InterpolationMode
linktitle: InterpolationMode
articleTitle: InterpolationMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GraphicsQualityOptions InterpolationMode, чтобы легко настроить параметры интерполяции графики для улучшения визуального качества.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Возвращает или задает режим интерполяции, связанный с этим Graphics.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

## Примеры

Показывает, как задать параметры качества рендеринга при преобразовании документов в форматы изображений.

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
