---
title: StringFormat
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает информацию о макете текста например выравнивание ориентация и позиции табуляции операции отображения например вставка многоточия и замена национальных цифр и функции OpenType.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Получает или задает информацию о макете текста (например, выравнивание, ориентация и позиции табуляции), операции отображения (например, вставка многоточия и замена национальных цифр) и функции OpenType.

```csharp
public StringFormat StringFormat { get; set; }
```

### Примеры

Показывает, как установить параметры качества рендеринга при преобразовании документов в форматы изображений.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions)
* пространство имен [Aspose.Words.Saving](../../graphicsqualityoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
