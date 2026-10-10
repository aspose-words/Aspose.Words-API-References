---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg yöntemi"
linktitle: "get_ExportEmbeddedSvg"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg yöntemi. SVG kaynaklarının Html belgesine gömülüp gömülmeyeceğini belirtir. Varsayılan değer C++'da true'dur."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


SVG kaynaklarının HTML belgesine gömülüp gömülmeyeceğini belirtir. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Örnekler



Bir belgeyi Html'ye dışa aktarırken SVG nesnelerinin nerede saklanacağını nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// SVG nesneleri içeren bir belgeyi .html'ye dışa aktardığımızda,
// Aspose.Words bu nesneleri iki olası konuma yerleştirebilir.
// \"ExportEmbeddedSvg\" bayrağını \"true\" olarak ayarlamak, tüm SVG nesne ham verilerini gömecek
// çıktı HTML içinde, <image> etiketleri içinde.
// Bu bayrağı \"false\" olarak ayarlamak, her SVG nesnesi için yerel dosya sisteminde bir dosya oluşturacaktır.
// HTML, her dosyaya bir <object> etiketinin \"data\" özniteliğini kullanarak bağlayacaktır.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
