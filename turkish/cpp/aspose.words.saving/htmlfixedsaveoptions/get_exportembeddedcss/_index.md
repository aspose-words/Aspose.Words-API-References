---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss yöntemi"
linktitle: "get_ExportEmbeddedCss"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss yöntemi. CSS (Cascading Style Sheet)'in Html belgesine C++'ta gömülüp gömülmeyeceğini belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


CSS (Cascading [Style](../../../aspose.words/style/) Sheet)'in Html belgesine gömülüp gömülmeyeceğini belirtir.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Örnekler



Bir belgeyi Html'ye dışa aktarırken CSS stil sayfalarının nerede depolanacağını nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir belgeyi html'ye dışa aktardığımızda, Aspose.Words belgeyi biçimlendirmek için bir CSS stil sayfası da oluşturur.
// \"ExportEmbeddedCss\" bayrağını \"true\" olarak ayarlamak, CSS stil sayfasını bir .css dosyasına kaydeder,
// ve html belgesinden <link> öğesini kullanarak dosyaya bağlanır.
// Bayrağı \"false\" olarak ayarlamak, CSS stil sayfasını Html belgesi içine gömer,
// bu da iki dosya yerine yalnızca bir dosya oluşturur.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
