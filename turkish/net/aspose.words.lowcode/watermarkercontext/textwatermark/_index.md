---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: .NET için Aspose.Words
description: İçeriğinizin güvenliğini ve markasını geliştirmek için özelleştirilebilir metin filigranlarını kolayca eklemek üzere WatermarkerContext TextWatermark özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Filigran olarak kullanılacak metin.

```csharp
public string TextWatermark { get; set; }
```

## Notlar

Eğer her ikisi de[`ImageWatermark`](../imagewatermark/) Ve`TextWatermark` belirtildiğinde, metin filigranı resim filigranını geçersiz kılar.

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

* class [WatermarkerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
