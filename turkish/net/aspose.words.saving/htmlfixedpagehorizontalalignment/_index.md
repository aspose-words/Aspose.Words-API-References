---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: .NET için Aspose.Words
description: HTML belgelerinizdeki sayfa hizalamasının hassas kontrolü için Aspose.Words.HtmlFixedPageHorizontalAlignment enum'unu keşfedin. Belge biçimlendirmenizi bugün geliştirin!
type: docs
weight: 5820
url: /tr/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Çıkış HTML belgesindeki sayfalar için yatay hizalamayı belirtir.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Sayfaları sola hizala. |
| Center | `1` | Sayfaları ortala. Bu varsayılan değerdir. |
| Right | `2` | Sayfaları sağa hizala. |

## Örnekler

Bir belgeyi HTML olarak kaydederken sayfaların yatay hizalamasının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
