---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GraphicsQualityOptions StringFormat для улучшенного управления макетом текста, включая выравнивание, многоточие и функции OpenType для лучшего отображения.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Возвращает или задает информацию о макете текста (например, выравнивание, ориентация и позиции табуляции), манипуляции с отображением (например, вставка многоточия и замена национальных цифр) и функции OpenType.

```csharp
public StringFormat StringFormat { get; set; }
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
