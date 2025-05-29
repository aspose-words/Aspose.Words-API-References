---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words для .NET
description: Оптимизируйте графику с помощью свойства ImageSaveOptions GraphicsQualityOptions, включающего точные режимы рендеринга и превосходное качество для создания потрясающих визуальных эффектов.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Позволяет указать режим и качество рендеринга дляGraphics объект.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Примечания

Используйте это свойство для переопределения настроек графики, предоставляемых движком Aspose.Words по умолчанию.

Он вступит в силу только при сохранении документа в формате, похожем на изображение.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
