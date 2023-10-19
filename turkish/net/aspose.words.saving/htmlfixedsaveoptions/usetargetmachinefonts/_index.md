---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions UseTargetMachineFonts mülk. Bayrak belgeyi görüntülemek için hedef makinedeki yazı tiplerinin kullanılması gerekip gerekmediğini belirtir. Bu bayrak olarak ayarlanırsadoğru FontFormat VeExportEmbeddedFonts özelliklerin etkisi yoktur ayrıcaResourceSavingCallback yazı tipleri için tetiklenmez. VarsayılanYANLIŞ  C#'da.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Bayrak, belgeyi görüntülemek için hedef makinedeki yazı tiplerinin kullanılması gerekip gerekmediğini belirtir. Bu bayrak, olarak ayarlanırsa`doğru` ,[`FontFormat`](../fontformat/) Ve[`ExportEmbeddedFonts`](../exportembeddedfonts/) özelliklerin etkisi yoktur, ayrıca[`ResourceSavingCallback`](../resourcesavingcallback/) yazı tipleri için tetiklenmez. Varsayılan:`YANLIŞ` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

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

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
