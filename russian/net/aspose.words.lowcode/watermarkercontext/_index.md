---
title: WatermarkerContext Class
linktitle: WatermarkerContext
articleTitle: WatermarkerContext
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.LowCode.WatermarkerContext для бесшовного нанесения водяных знаков на документы. Улучшайте свои документы с легкостью и эффективностью.
type: docs
weight: 4450
url: /ru/net/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class

Контекст водяного знака документа.

```csharp
public class WatermarkerContext : ProcessorContext
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [WatermarkerContext](watermarkercontext/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Настройки шрифта, используемые процессором. |
| [ImageWatermark](../../aspose.words.lowcode/watermarkercontext/imagewatermark/) { get; set; } | Байты изображения, которые будут использоваться в качестве водяного знака. |
| [ImageWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/) { get; } | Варианты текстового водяного знака. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Параметры макета документа, используемые процессором. |
| [TextWatermark](../../aspose.words.lowcode/watermarkercontext/textwatermark/) { get; set; } | Текст, который будет использоваться в качестве водяного знака. |
| [TextWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/textwatermarkoptions/) { get; } | Варианты водяного знака изображения. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Предупреждающий обратный вызов, используемый процессором. |

## Примеры

Показывает, как вставить текст водяного знака в документ с использованием контекста.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Показывает, как вставить изображение водяного знака в документ с использованием контекста.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

Показывает, как вставить текст водяного знака в документ из потока с использованием контекста.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

Показывает, как вставить изображение водяного знака в документ из потока с использованием контекста.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* class [ProcessorContext](../processorcontext/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
