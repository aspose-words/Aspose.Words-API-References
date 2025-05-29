---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: .NET için Aspose.Words
description: HTML sabit formatına dönüştürürken en iyi font dışa aktarımı için Aspose.Words.Saving.ExportFontFormat enum'unu keşfedin. Belgenizin görsel kalitesini artırın!
type: docs
weight: 5740
url: /tr/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

HTML sabit biçimine dönüştürülürken yazı tiplerini dışa aktarmak için kullanılan biçimi belirtir.

```csharp
public enum ExportFontFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Woff | `0` | WOFF (Web Açık Yazı Tipi Biçimi). |
| Ttf | `1` | TTF (TrueType Yazı Tipi biçimi). |

## Örnekler

Bir belgeyi HTML'e kaydederken yalnızca hedef makinedeki yazı tiplerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Ayrıca bakınız

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
