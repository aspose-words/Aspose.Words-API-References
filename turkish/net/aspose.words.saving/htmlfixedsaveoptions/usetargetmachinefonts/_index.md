---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions'daki UseTargetMachineFonts özelliğinin hedef makine yazı tiplerini kullanarak belge görüntülemesini nasıl geliştirdiğini keşfedin. Yazı tipi yönetiminizi bugün optimize edin!
type: docs
weight: 210
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Bayrağı, hedef makinedeki yazı tiplerinin belgeyi görüntülemek için kullanılıp kullanılmayacağını belirtir. Bu bayrak,`doğru` ,[`FontFormat`](../fontformat/) Ve[`ExportEmbeddedFonts`](../exportembeddedfonts/) özelliklerin etkisi yoktur, ayrıca[`ResourceSavingCallback`](../resourcesavingcallback/) fontlar için ateşlenmez. Varsayılan`YANLIŞ` .

```csharp
public bool UseTargetMachineFonts { get; set; }
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

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
