---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words для .NET
description: Откройте для себя настраиваемые параметры водяных знаков изображений с помощью свойства WatermarkerContext TextWatermarkOptions, чтобы улучшить визуальные эффекты и защитить контент.
type: docs
weight: 50
url: /ru/net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Варианты водяного знака изображения.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

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

### Смотрите также

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
