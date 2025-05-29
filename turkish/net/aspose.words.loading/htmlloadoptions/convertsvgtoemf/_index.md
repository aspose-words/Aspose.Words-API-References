---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: .NET için Aspose.Words
description: HtmlLoadOptions' ConvertSvgToEmf özelliğini keşfedin. En iyi görüntü kalitesi için SVG'den EMF'ye dönüştürmeyi kolayca kontrol edin. Varsayılan false'tur; SVG'leri olduğu gibi bırakın!
type: docs
weight: 30
url: /tr/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Yüklenen SVG resimlerinin EMF biçimine dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` ve mümkünse, yüklenen SVG görüntüleri dönüştürülmeden olduğu gibi saklanır.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Notlar

MS Word'ün daha yeni sürümleri SVG resimlerini doğal olarak destekler. Yükleme seçeneklerinde belirtilen MS Word sürümü SVG'yi destekliyorsa, Aspose.Words SVG resimlerini dönüştürmeden olduğu gibi depolayacaktır. SVG desteklenmiyorsa, yüklenen SVG resimleri EMF biçimine dönüştürülecektir.

Ancak bu seçenek şu şekilde ayarlanırsa:`doğru` , Aspose.Words, SVG görüntüleri belirtilen MS Word sürümü tarafından desteklense bile yüklenen SVG görüntülerini EMF'ye dönüştürecektir.

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

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
