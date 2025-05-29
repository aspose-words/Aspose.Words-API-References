---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.GraphicsQualityOptions, который позволяет улучшить качество графики документа с помощью настраиваемых параметров для превосходного вывода.
type: docs
weight: 5790
url: /ru/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Позволяет указать дополнительныеGraphics параметры качества.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class GraphicsQualityOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Возвращает или задает значение, указывающее, как составные изображения отображаются в этом Graphics. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Возвращает или задает качество рендеринга составных изображений, нарисованных в этом Graphics. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Возвращает или задает режим интерполяции, связанный с этим Graphics. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Получает или задает качество рендеринга для этого Graphics. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Возвращает или задает информацию о макете текста (например, выравнивание, ориентация и позиции табуляции), манипуляции с отображением (например, вставка многоточия и замена национальных цифр) и функции OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Возвращает или задает режим рендеринга для текста, связанного с этим Graphics. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Возвращает или задает флаг, указывающий, является ли WrapMode TileFlipXY. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
