---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. SVG kaynaklarının Html belgesine gömülmesi gerekip gerekmediğini belirtir. Varsayılan değerdoğru .
type: docs
weight: 70
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

SVG kaynaklarının Html belgesine gömülmesi gerekip gerekmediğini belirtir. Varsayılan değer`doğru` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

### Örnekler

Bir belgeyi Html'e aktarırken SVG nesnelerinin nerede saklanacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// SVG nesneleri içeren bir belgeyi .html'ye aktardığımızda,
// Aspose.Words bu nesneleri iki olası konuma yerleştirebilir.
// "ExportEmbeddedSvg" bayrağının "true" olarak ayarlanması, tüm SVG nesnesi ham verilerini gömecektir
// çıktı HTML'sinin içinde, <image> etiketler.
// Bu bayrağı "false" olarak ayarlamak, her SVG nesnesi için yerel dosya sisteminde bir dosya oluşturacaktır.
// HTML, bir <object> etiket.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


