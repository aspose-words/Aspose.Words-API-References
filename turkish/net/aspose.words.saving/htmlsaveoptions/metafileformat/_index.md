---
title: HtmlSaveOptions.MetafileFormat
linktitle: MetafileFormat
articleTitle: MetafileFormat
second_title: Aspose.Words for .NET
description: HtmlSaveOptions MetafileFormat mülk. HTML MHTML veya EPUBa dışa aktarırken meta dosyalarının hangi formatta kaydedileceğini belirtir. Varsayılan değerPng  meta dosyalarının PNG görüntülerine raster olarak işlendiği anlamına gelir C#'da.
type: docs
weight: 380
url: /tr/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

HTML, MHTML veya EPUB'a dışa aktarırken meta dosyalarının hangi formatta kaydedileceğini belirtir. Varsayılan değer:Png , meta dosyalarının PNG görüntülerine raster olarak işlendiği anlamına gelir.

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

## Notlar

Meta dosyalar orijinal olarak HTML tarayıcıları tarafından görüntülenmez. Aspose.Words, HTML'ye dışa aktarırken varsayılan olarak WMF ve EMF görüntülerini PNG dosyalarına dönüştürür. Diğer seçenekler meta dosyalarını SVG görüntülerine dönüştürmek veya bunları dönüştürme olmadan olduğu gibi dışa aktarmaktır.

Bazı görüntü dönüştürmeleri, özellikle görüntü kırpma, eğer onlar dönüştürme olmadan HTML'ye aktarılırsa meta dosyası görüntülerine uygulanmayacaktır.

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

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
