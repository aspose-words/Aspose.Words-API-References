---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: .NET için Aspose.Words
description: Gelişmiş görsel kalite ve özelleştirme için SVG'de metin oluşturmayı kontrol eden SvgSaveOptions TextOutputMode özelliğini keşfedin. Grafiklerinizi bugün optimize edin!
type: docs
weight: 120
url: /tr/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Metnin SVG'de nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Notlar

Bu özelliği, bir belgenin içindeki metnin SVG biçiminde kaydedilirken nasıl rendered olacağını belirlemek veya almak için kullanın.

Varsayılan değer:UseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
