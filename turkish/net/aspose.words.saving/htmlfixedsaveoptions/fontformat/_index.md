---
title: HtmlFixedSaveOptions.FontFormat
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Alır veya ayarlarExportFontFormat yazı tipi dışa aktarma için kullanılır. Varsayılan değerWoff .
type: docs
weight: 90
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Alır veya ayarlar[`ExportFontFormat`](../../exportfontformat/) yazı tipi dışa aktarma için kullanılır. Varsayılan değerWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

### Örnekler

Bir belgeyi HTML'ye kaydederken yazı tiplerinin yalnızca hedef makineden nasıl kullanıldığını gösterir.

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
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


