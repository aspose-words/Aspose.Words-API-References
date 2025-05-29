---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: .NET için Aspose.Words
description: ExportEmbeddedFonts özelliğiyle HTML'nize font yerleştirmeyi kontrol edin. Dosya boyutunu etkili bir şekilde yönetirken belge kalitesini artırın.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Yazı tiplerinin Base64 biçiminde Html belgesine gömülmesi gerekip gerekmediğini belirtir. Bu bayrağı ayarlamanın çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Örnekler

Bir belgeyi HTML'ye aktarırken gömülü yazı tiplerinin nereye kaydedileceğinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Gömülü yazı tiplerine sahip bir belgeyi .html'ye aktardığımızda,
// Aspose.Words yazı tiplerini iki olası yere yerleştirebilir.
// "ExportEmbeddedFonts" bayrağını "true" olarak ayarlamak, gömülü fontların ham verilerini CSS stil sayfasında saklayacaktır.
// "@font-face" kuralının "url" özelliğinde. Bu, büyük bir CSS stil dosyası oluşturabilir
// ve bu HTML dönüşümünün oluşturacağı harici dosyaların sayısını azaltın.
// Bu bayrağı "false" olarak ayarlamak her yazı tipi için bir dosya oluşturacaktır.
// CSS stil sayfası, "@font-face" kuralının "url" özelliğini kullanarak her yazı tipi dosyasına bağlantı verecektir.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
