---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat metodu"
linktitle: "get_FontFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat metodu. Yazı tipi dışa aktarma için kullanılan ExportFontFormat değerini alır veya ayarlar. Varsayılan değer C++'ta Woff'tur."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_fontformat/
---
## HtmlFixedSaveOptions::get_FontFormat method


[ExportFontFormat](../../exportfontformat/) yazı tipi dışa aktarma için kullanılan değerini alır veya ayarlar. Varsayılan değer [Woff](../../exportfontformat/)'dır.

```cpp
Aspose::Words::Saving::ExportFontFormat Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat() const
```


## Örnekler



Bir belgeyi HTML olarak kaydederken yalnızca hedef makinedeki yazı tiplerinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bullet points with alternative font.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(Aspose::Words::Saving::ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") + u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")->get_Success());
}
```

## Ayrıca Bakınız

* Enum [ExportFontFormat](../../exportfontformat/)
* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
