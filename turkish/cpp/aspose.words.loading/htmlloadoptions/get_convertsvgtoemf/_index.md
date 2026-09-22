---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf yöntemi"
linktitle: "get_ConvertSvgToEmf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf yöntemi. Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini belirten bir değeri alır veya ayarlar. Varsayılan değer false'tur ve mümkün olduğunda, yüklenen SVG görüntüleri dönüşüm olmadan olduğu gibi C++'de saklanır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini gösteren bir değeri alır veya ayarlar. Varsayılan değer **false**'dur ve mümkün olduğunda, yüklenen SVG görüntüleri dönüşüm olmadan olduğu gibi depolanır.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## Açıklamalar


MS Word'ün daha yeni sürümleri SVG görüntülerini yerel olarak destekler. Yükleme seçeneklerinde belirtilen MS Word sürümü SVG'yi destekliyorsa, Aspose.Words SVG görüntülerini olduğu gibi dönüşüm olmadan saklayacaktır. SVG desteklenmiyorsa, yüklenen SVG görüntüleri EMF formatına dönüştürülecektir.

Ancak, bu seçenek **true** olarak ayarlanırsa, Aspose.Words belirtilen MS Word sürümü SVG görüntülerini desteklese bile yüklenen SVG görüntülerini EMF'ye dönüştürecektir.

## Örnekler



HTML belgeleri kaydedilirken SVG nesnelerinin farklı bir biçime nasıl dönüştürüleceğini gösterir.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// 'ConvertSvgToEmf' kullanarak eski davranışı geri döndürün
// burada bir HTML belgesinden yüklenen tüm SVG görüntüleri EMF'ye dönüştürülmüştü.
// Artık SVG görüntüler dönüşüm olmadan yüklenir
// yükleme seçeneklerinde belirtilen MS Word sürümü SVG görüntülerini yerel olarak destekliyorsa.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Bu belge, metin biçiminde bir <svg> öğesi içerir.
// Belgeyi HTML olarak kaydettiğimizde, bir SaveOptions nesnesi geçebiliriz.
// kaydetme işleminin bu nesneyi nasıl işlediğini belirlemek için.
// "MetafileFormat" özelliğini "HtmlMetafileFormat.Png" olarak ayarlayarak PNG görüntüsüne dönüştürmek.
// "MetafileFormat" özelliğini "HtmlMetafileFormat.Svg" olarak ayarlayarak bir SVG nesnesi olarak korumak.
// "MetafileFormat" özelliğini "HtmlMetafileFormat.EmfOrWmf" olarak ayarlayarak bir metafile'a dönüştürmek.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## Ayrıca Bakınız

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
