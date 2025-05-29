---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: .NET için Aspose.Words
description: SVG formatında metin oluşturmayı özelleştirmek, belge sunumunu ve görsel çekiciliği geliştirmek için Aspose.Words.Saving.SvgTextOutputMode enum'unu keşfedin.
type: docs
weight: 6410
url: /tr/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Bir belgenin içindeki metnin SVG biçiminde kaydedilirken nasıl işleneceğini belirtmeye izin verir.

```csharp
public enum SvgTextOutputMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG yazı tipleri metin oluşturmak için kullanılır. Tüm tarayıcıların SVG yazı tiplerini desteklemediğini unutmayın. |
| UseTargetMachineFonts | `1` | Hedef makineye yüklenen yazı tipleri metin oluşturmak için kullanılır. Not: Belgede kullanılan yazı tiplerinden bazıları hedef makinede mevcut değilse, belge farklı görünebilir. |
| UsePlacedGlyphs | `2` | Metin eğriler kullanılarak işlenir. Bu seçeneği kullanırsanız metin seçiminin çalışmayacağını unutmayın. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
