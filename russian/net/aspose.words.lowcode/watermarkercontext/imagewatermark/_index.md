---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words для .NET
description: Узнайте, как улучшить изображения с помощью свойства WatermarkerContext ImageWatermark, позволяющего без труда добавлять пользовательские изображения водяных знаков.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Байты изображения, которые будут использоваться в качестве водяного знака.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Примечания

Если оба`ImageWatermark` и[`TextWatermark`](../textwatermark/) указаны, текстовый водяной знак переопределяет водяной знак изображения.

## Примеры

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

* class [WatermarkerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
