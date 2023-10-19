---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ExportFontFormat Sıralama. Sabit HTML biçimine dönüştürülürken yazı tiplerini dışa aktarmak için kullanılan biçimi belirtir C#'da.
type: docs
weight: 4990
url: /tr/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Sabit HTML biçimine dönüştürülürken yazı tiplerini dışa aktarmak için kullanılan biçimi belirtir.

```csharp
public enum ExportFontFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Woff | `0` | WOFF (Web Açık Yazı Tipi Formatı). |
| Ttf | `1` | TTF (TrueType Yazı Tipi formatı). |

## Örnekler

Bir belgeyi HTML'ye kaydederken yazı tiplerinin yalnızca hedef makineden nasıl kullanılacağını gösterir.

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
