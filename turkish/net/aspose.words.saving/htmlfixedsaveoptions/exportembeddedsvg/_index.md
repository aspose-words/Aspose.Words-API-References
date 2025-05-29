---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions' ExportEmbeddedSvg özelliğini keşfedin, gelişmiş görseller için SVG kaynaklarını HTML belgelerinize kolayca gömün. Varsayılan, true.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

SVG kaynaklarının Html belgesine gömülüp gömülmeyeceğini belirtir. Varsayılan değer`doğru` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Örnekler

Bir belgeyi HTML'ye aktarırken SVG nesnelerinin nereye kaydedileceğinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// SVG nesneleri içeren bir belgeyi .html'ye aktardığımızda,
// Aspose.Words bu nesneleri iki olası konuma yerleştirebilir.
// "ExportEmbeddedSvg" bayrağını "true" olarak ayarlamak tüm SVG nesnesinin ham verilerini gömecektir
// çıktı HTML'inin içinde, <image> etiketlerinin içinde.
// Bu bayrağı "false" olarak ayarlamak, her SVG nesnesi için yerel dosya sisteminde bir dosya oluşturacaktır.
// HTML, her dosyaya <object> etiketinin "data" niteliğini kullanarak bağlantı verecektir.
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
