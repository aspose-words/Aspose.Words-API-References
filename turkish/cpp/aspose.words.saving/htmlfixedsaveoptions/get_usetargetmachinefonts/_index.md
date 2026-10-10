---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts yöntemi"
linktitle: "get_UseTargetMachineFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts yöntemi. Bayrak, hedef makineden gelen yazı tiplerinin belgeyi görüntülemek için kullanılmasını gösterir. Bu bayrak true olarak ayarlanırsa, FontFormat ve ExportEmbeddedFonts özellikleri etkili olmaz, ayrıca ResourceSavingCallback yazı tipleri için tetiklenmez. Varsayılan değer false'tur C++'de."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Bayrak, hedef makineden gelen yazı tiplerinin belgeyi görüntülemek için kullanılıp kullanılmayacağını gösterir. Bu bayrak **true** olarak ayarlanırsa, [FontFormat](../get_fontformat/) ve [ExportEmbeddedFonts](../get_exportembeddedfonts/) özellikleri etkili olmaz, ayrıca [ResourceSavingCallback](../get_resourcesavingcallback/) yazı tipleri için tetiklenmez. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
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

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
