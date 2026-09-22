---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages yöntemi"
linktitle: "get_ExportEmbeddedImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages yöntemi. Görsellerin Html belgesine Base64 biçiminde gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının C++'ta çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Görsellerin HTML belgesine Base64 biçiminde gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının çıktı HTML dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Örnekler



Bir belgeyi Html'ye dışa aktarırken görsellerin nerede depolanacağını nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Gömülü görselleri içeren bir belgeyi .html'ye dışa aktardığımızda,
// Aspose.Words görselleri iki olası konuma yerleştirebilir.
// \"ExportEmbeddedImages\" bayrağını \"true\" olarak ayarlamak, ham veriyi depolar
// çıktı HTML belgesindeki tüm görseller için, <image> etiketlerinin \"src\" özniteliğinde.
// Bu bayrağı \"false\" olarak ayarlamak, her görsel için yerel dosya sisteminde bir görsel dosyası oluşturur,
// ve bu dosyaların tümünü ayrı bir klasörde depolar.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
