---
title: HtmlFixedSaveOptions.FontFormat
linktitle: FontFormat
articleTitle: FontFormat
second_title: .NET için Aspose.Words
description: Yazı tipi dışa aktarmayı özelleştirmek için HtmlFixedSaveOptions FontFormat özelliğini keşfedin. Daha iyi performans için varsayılan biçiminizi Woff olarak kolayca ayarlayın ve optimize edin.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Alır veya ayarlar[`ExportFontFormat`](../../exportfontformat/) yazı tipi dışa aktarımı için kullanılır. Varsayılan değerWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

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

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
