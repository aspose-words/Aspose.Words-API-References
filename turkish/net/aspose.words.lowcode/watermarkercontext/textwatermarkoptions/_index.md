---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: .NET için Aspose.Words
description: Görsellerinizi geliştirmek ve içeriğinizi korumak için WatermarkerContext TextWatermarkOptions özelliğiyle resim filigranları için özelleştirilebilir seçenekleri keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Resim filigranı için seçenekler.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

## Örnekler

Bağlam kullanılarak belgeye filigran metninin nasıl ekleneceğini gösterir.

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

Akıştan belgeye filigran metninin nasıl ekleneceğini bağlam kullanarak gösterir.

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

### Ayrıca bakınız

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
