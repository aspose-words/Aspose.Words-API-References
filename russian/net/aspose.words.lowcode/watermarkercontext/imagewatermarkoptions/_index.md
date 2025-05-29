---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words для .NET
description: Откройте для себя настраиваемые параметры текстового водяного знака с помощью WatermarkerContext, чтобы улучшить ваши изображения и эффективно защитить индивидуальность вашего бренда.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Варианты текстового водяного знака.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; }
```

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

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
