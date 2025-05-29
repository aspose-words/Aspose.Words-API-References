---
title: WatermarkerContext Class
linktitle: WatermarkerContext
articleTitle: WatermarkerContext
second_title: .NET için Aspose.Words
description: Kusursuz belge filigranlama için Aspose.Words.LowCode.WatermarkerContext sınıfını keşfedin. Belgelerinizi kolaylıkla ve etkili bir şekilde geliştirin.
type: docs
weight: 4450
url: /tr/net/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class

Belge filigran bağlamı.

```csharp
public class WatermarkerContext : ProcessorContext
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [WatermarkerContext](watermarkercontext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [ImageWatermark](../../aspose.words.lowcode/watermarkercontext/imagewatermark/) { get; set; } | Filigran olarak kullanılacak resim baytları. |
| [ImageWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/) { get; } | Metin filigranı için seçenekler. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [TextWatermark](../../aspose.words.lowcode/watermarkercontext/textwatermark/) { get; set; } | Filigran olarak kullanılacak metin. |
| [TextWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/textwatermarkoptions/) { get; } | Resim filigranı için seçenekler. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | İşlemci tarafından kullanılan uyarı geri araması. |

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

* class [ProcessorContext](../processorcontext/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
