---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: .NET için Aspose.Words
description: HTML belgelerinde kusursuz meta dosyası kaydı için Aspose.Words.Saving.HtmlMetafileFormat enum'unu keşfedin. Belge dönüştürme deneyiminizi bugün geliştirin!
type: docs
weight: 5840
url: /tr/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

Meta dosyalarının HTML belgelerine kaydedildiği biçimi belirtir.

```csharp
public enum HtmlMetafileFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Png | `0` | Meta dosyaları raster PNG görüntülerine dönüştürülür. |
| Svg | `1` | Meta dosyaları vektör SVG görüntülerine dönüştürülür. |
| EmfOrWmf | `2` | Meta dosyaları dönüştürülmeden olduğu gibi kaydedilir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
