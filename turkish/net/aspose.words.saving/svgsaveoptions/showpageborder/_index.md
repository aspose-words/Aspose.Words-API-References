---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: .NET için Aspose.Words
description: Sayfa anahatlarınızı özelleştirmek için SvgSaveOptions ShowPageBorder özelliğini keşfedin. Kenarlıkları zahmetsizce kontrol edin—kolay kullanım için varsayılan ayar true'dur!
type: docs
weight: 110
url: /tr/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Sayfanın ana hatlarına bir kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılan`doğru` .

```csharp
public bool ShowPageBorder { get; set; }
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
