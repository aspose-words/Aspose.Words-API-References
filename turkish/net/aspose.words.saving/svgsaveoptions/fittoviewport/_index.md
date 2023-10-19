---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words for .NET
description: SvgSaveOptions FitToViewPort mülk. Çıkış SVGsinin mevcut görünüm alanını tarayıcı penceresi veya kapsayıcı doldurması gerekip gerekmediğini belirtir. Olarak ayarlandığındadoğru SVG çıkışının genişliği ve yüksekliği 100 olarak ayarlandı C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Çıkış SVG'sinin mevcut görünüm alanını (tarayıcı penceresi veya kapsayıcı) doldurması gerekip gerekmediğini belirtir. Olarak ayarlandığında`doğru` SVG çıkışının genişliği ve yüksekliği %100 olarak ayarlandı.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool FitToViewPort { get; set; }
```

## Örnekler

Bir .docx belgesini .svg'ye dönüştürürken görüntülerin özelliklerinin nasıl taklit edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// SvgSaveOptions nesnesini, sayfa kenarlıkları veya seçilebilir metin olmadan kaydedilecek şekilde yapılandırın.
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
