---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: .NET için Aspose.Words
description: Resimlerinizi WatermarkerContext ImageWatermark özelliğiyle nasıl geliştirebileceğinizi keşfedin; bu özellik sayesinde özel filigran resimlerinizi zahmetsizce ekleyebilirsiniz.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Filigran olarak kullanılacak resim baytları.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Notlar

Eğer her ikisi de`ImageWatermark` Ve[`TextWatermark`](../textwatermark/) belirtildiğinde, metin filigranı resim filigranını geçersiz kılar.

## Örnekler

Bağlam kullanılarak belgeye filigran resminin nasıl ekleneceğini gösterir.

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

Bağlam kullanılarak bir akıştan belgeye filigran resminin nasıl ekleneceğini gösterir.

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

### Ayrıca bakınız

* class [WatermarkerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
