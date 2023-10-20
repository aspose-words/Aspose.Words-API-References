---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words for .NET
description: HtmlLoadOptions ConvertSvgToEmf mülk. Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değerYANLIŞ ve mümkünse yüklenen SVG görüntüleri dönüştürme yapılmadan olduğu gibi depolanır C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer:`YANLIŞ` ve mümkünse yüklenen SVG görüntüleri dönüştürme yapılmadan olduğu gibi depolanır.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Notlar

MS Word'ün daha yeni sürümleri, SVG resimlerini yerel olarak destekler. Yükleme seçeneklerinde belirtilen MS Word sürümü SVG'yi destekliyorsa Aspose.Words, SVG görüntülerini dönüştürme olmadan olduğu gibi saklar. SVG desteklenmiyorsa yüklenen SVG görüntüleri EMF formatına dönüştürülecektir.

Ancak bu seçenek şu şekilde ayarlanmışsa:`doğru` , Aspose.Words, SVG görselleri MS Word'ün belirtilen sürümü tarafından desteklense bile, yüklenen SVG görsellerini EMF'ye dönüştürecektir.

## Örnekler

HTML belgelerini kaydederken SVG nesnelerinin farklı bir formata nasıl dönüştürüleceğini gösterir.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Eski davranışı geri döndürmek için 'ConvertSvgToEmf'i kullanın
// burada bir HTML belgesinden yüklenen tüm SVG görüntüleri EMF'ye dönüştürüldü.
// Artık SVG görselleri dönüştürme yapılmadan yükleniyor
// yükleme seçeneklerinde belirtilen MS Word sürümü SVG resimlerini yerel olarak destekliyorsa.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Bu belge bir <svg> metin biçiminde öğe.
// Belgeyi HTML'ye kaydettiğimizde SaveOptions nesnesini iletebiliriz
// kaydetme işleminin bu nesneyi nasıl işleyeceğini belirlemek için.
// PNG görüntüsüne dönüştürmek için "MetafileFormat" özelliğini "HtmlMetafileFormat.Png" olarak ayarlıyoruz.
// "MetafileFormat" özelliğinin "HtmlMetafileFormat.Svg" olarak ayarlanması onu bir SVG nesnesi olarak korur.
// Bir meta dosyasına dönüştürmek için "MetafileFormat" özelliğini "HtmlMetafileFormat.EmfOrWmf" olarak ayarlıyoruz.
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
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height= \"40\">"));
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
