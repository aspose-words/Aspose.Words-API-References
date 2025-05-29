---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: .NET için Aspose.Words
description: SvgSaveOptions FitToViewPort özelliğinin, SVG çıktınızı herhangi bir tarayıcı penceresini veya kapsayıcısını mükemmel şekilde dolduracak şekilde nasıl optimize ettiğini ve çarpıcı görseller sunduğunu keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Çıktı SVG'sinin kullanılabilir görüntüleme alanını (tarayıcı penceresi veya kapsayıcı) doldurup doldurmayacağını belirtir. olarak ayarlandığında`doğru`çıktı SVG'sinin genişliği ve yüksekliği %100 olarak ayarlandı.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool FitToViewPort { get; set; }
```

## Örnekler

.docx belgesini .svg'ye dönüştürürken görsellerin özelliklerinin nasıl taklit edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// SvgSaveOptions nesnesini sayfa kenarlıkları veya seçilebilir metin olmadan kaydedecek şekilde yapılandırın.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
