---
title: GraphicsQualityOptions.TextRenderingHint
linktitle: TextRenderingHint
articleTitle: TextRenderingHint
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GraphicsQualityOptions TextRenderingHint для оптимальной визуализации текста в вашей графике. Улучшите визуальное качество и производительность сегодня!
type: docs
weight: 70
url: /ru/net/aspose.words.saving/graphicsqualityoptions/textrenderinghint/
---
## GraphicsQualityOptions.TextRenderingHint property

Возвращает или задает режим рендеринга для текста, связанного с этим Graphics.

```csharp
public TextRenderingHint? TextRenderingHint { get; set; }
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
