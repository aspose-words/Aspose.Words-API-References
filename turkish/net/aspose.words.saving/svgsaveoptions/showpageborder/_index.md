---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words for .NET
description: SvgSaveOptions ShowPageBorder mülk. Sayfanın ana hatlarına kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılandoğru  C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Sayfanın ana hatlarına kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılan:`doğru` .

```csharp
public bool ShowPageBorder { get; set; }
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
