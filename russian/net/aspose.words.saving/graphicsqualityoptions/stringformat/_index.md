---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: Aspose.Words для .NET
description: GraphicsQualityOptions StringFormat свойство. Получает или задает информацию о макете текста например выравнивание ориентацию и позиции табуляции манипуляции с отображением например вставку многоточия и замену национальных цифр и функции OpenType на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Получает или задает информацию о макете текста (например, выравнивание, ориентацию и позиции табуляции), манипуляции с отображением (например, вставку многоточия и замену национальных цифр) и функции OpenType.

```csharp
public StringFormat StringFormat { get; set; }
```

## Примеры

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
