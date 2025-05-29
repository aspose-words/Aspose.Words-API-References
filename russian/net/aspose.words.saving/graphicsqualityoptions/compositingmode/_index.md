---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GraphicsQualityOptions CompositingMode, чтобы оптимизировать процесс рендеринга изображений, повысив производительность и качество графики.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Возвращает или задает значение, указывающее, как составные изображения отображаются в этом Graphics.

```csharp
public CompositingMode? CompositingMode { get; set; }
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
