---
title: UseTargetMachineFonts
second_title: Aspose.Words for .NET API Referansı
description: Bayrak belgeyi görüntülemek için hedef makinedeki yazı tiplerinin kullanılması gerekip gerekmediğini gösterir. Bu bayrak true olarak ayarlanırsaFontFormataspose.words.saving/htmlfixedsaveoptions/fontformat veExportEmbeddedFontsaspose.words.saving/htmlfixedsaveoptions/exportembeddedfontsözelliklerin etkisi yoktur ayrıcaResourceSavingCallbackaspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback yazı tipleri için tetiklenmedi. Varsayılan yanlıştır.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Bayrak, belgeyi görüntülemek için hedef makinedeki yazı tiplerinin kullanılması gerekip gerekmediğini gösterir. Bu bayrak true olarak ayarlanırsa,[`FontFormat`](../fontformat) ve[`ExportEmbeddedFonts`](../exportembeddedfonts)özelliklerin etkisi yoktur, ayrıca[`ResourceSavingCallback`](../resourcesavingcallback) yazı tipleri için tetiklenmedi. Varsayılan yanlıştır.

```csharp
public bool UseTargetMachineFonts { get; set; }
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

* class [HtmlFixedSaveOptions](../../htmlfixedsaveoptions)
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->