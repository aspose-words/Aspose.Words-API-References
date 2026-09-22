---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts yöntemi"
linktitle: "get_ExportEmbeddedFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts yöntemi. Yazı tiplerinin Html belgesine Base64 formatında gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının C++'da çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Yazı tiplerinin HTML belgesine Base64 biçiminde gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının çıktı HTML dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Örnekler



Bir belgeyi Html'ye dışa aktarırken gömülü yazı tiplerinin nerede saklanacağını nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Gömülü yazı tipleri içeren bir belgeyi .html'ye dışa aktardığımızda,
// Aspose.Words yazı tiplerini iki olası konuma yerleştirebilir.
// \"ExportEmbeddedFonts\" bayrağını \"true\" olarak ayarlamak, gömülü yazı tiplerinin ham verilerini CSS stil sayfası içinde saklayacaktır,
// \"@font-face\" kuralının \"url\" özelliğinde. Bu, büyük bir CSS stil sayfası dosyası oluşturabilir
// ve bu HTML dönüşümünün oluşturacağı dış dosya sayısını azaltır.
// Bu bayrağı "false" olarak ayarlamak, her yazı tipi için bir dosya oluşturur.
// CSS stil sayfası, "@font-face" kuralının "url" özelliğini kullanarak her yazı tipi dosyasına bağlanacaktır.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
