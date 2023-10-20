---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.SvgTextOutputMode Sıralama. SVG biçiminde kaydederken bir belge içindeki metnin nasıl işlenmesi gerektiğini belirlemeye olanak tanır  C#'da.
type: docs
weight: 5610
url: /tr/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

SVG biçiminde kaydederken bir belge içindeki metnin nasıl işlenmesi gerektiğini belirlemeye olanak tanır .

```csharp
public enum SvgTextOutputMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG yazı tipleri metin oluşturmak için kullanılır. Tüm tarayıcıların SVG yazı tiplerini desteklemediğini unutmayın. |
| UseTargetMachineFonts | `1` | Hedef makinede yüklü olan yazı tipleri, metni oluşturmak için kullanılır. Belgede kullanılan bazı yazı tiplerinin hedef makinede mevcut olmaması durumunda belgenin farklı görünebileceğini unutmayın. |
| UsePlacedGlyphs | `2` | Metin, eğriler kullanılarak oluşturulur. Bu seçeneği kullanırsanız metin seçiminin çalışmayacağını unutmayın. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
