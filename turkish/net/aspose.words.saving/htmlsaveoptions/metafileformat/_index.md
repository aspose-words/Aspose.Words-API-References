---
title: HtmlSaveOptions.MetafileFormat
linktitle: MetafileFormat
articleTitle: MetafileFormat
second_title: .NET için Aspose.Words
description: HTML, MHTML veya EPUB'a dışa aktarmak için HtmlSaveOptions MetafileFormat özelliğini keşfedin. Meta dosyalarını varsayılan olarak yüksek kaliteli PNG görüntüleri olarak kaydedin!
type: docs
weight: 380
url: /tr/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

HTML, MHTML veya EPUB'a aktarırken meta dosyalarının hangi biçimde kaydedileceğini belirtir. Varsayılan değerPng , meta dosyalarının raster PNG görüntülerine dönüştürüldüğü anlamına gelir.

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

## Notlar

Meta dosyaları HTML tarayıcıları tarafından doğal olarak görüntülenmez. Varsayılan olarak, Aspose.Words HTML'ye aktarırken WMF ve EMF resimlerini PNG dosyalarına dönüştürür. Diğer seçenekler meta dosyalarını SVG resimlerine dönüştürmek veya dönüştürmeden olduğu gibi export yapmaktır.

Bazı görüntü dönüşümleri, özellikle görüntü kırpma, dönüştürülmeden HTML'e aktarılırsa meta dosya görüntülerine uygulanmayacaktır.

## Örnekler

HTML belgelerini kaydederken SVG nesnelerinin farklı bir biçime nasıl dönüştürüleceğini gösterir.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' genişlik='500' yükseklik='40' görünümKutusu='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Eski davranışı geri döndürmek için 'ConvertSvgToEmf'yi kullanın
// HTML belgesinden yüklenen tüm SVG görsellerinin EMF'ye dönüştürüldüğü yer.
// Artık SVG görüntüleri dönüştürülmeden yükleniyor
// yükleme seçeneklerinde belirtilen MS Word sürümü SVG resimlerini doğal olarak destekliyorsa.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Bu belge metin biçiminde bir <svg> öğesi içeriyor.
// Belgeyi HTML'e kaydettiğimizde, SaveOptions nesnesini geçirebiliriz
// kaydetme işleminin bu nesneyi nasıl işleyeceğini belirlemek için.
// PNG resmine dönüştürmek için "MetafileFormat" özelliğini "HtmlMetafileFormat.Png" olarak ayarlıyoruz.
// "MetafileFormat" özelliğini "HtmlMetafileFormat.Svg" olarak ayarlayarak SVG nesnesi olarak saklayabiliriz.
// "MetafileFormat" özelliğini meta dosyasına dönüştürmek için "HtmlMetafileFormat.EmfOrWmf" olarak ayarlıyoruz.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" sürüm=\"1.1\" genişlik=\"499\" yükseklik=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Ayrıca bakınız

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
