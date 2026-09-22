---
title: "Aspose::Words::Saving::ExportFontFormat enum"
linktitle: "ExportFontFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ExportFontFormat enum. C++'ta HTML sabit formatına render edilirken yazı tiplerini dışa aktarmak için kullanılan formatı gösterir."
type: docs
weight: 54000
url: /tr/cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


HTML sabit formatına işlenirken yazı tiplerini dışa aktarmak için kullanılan formatı gösterir.

```cpp
enum class ExportFontFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Woff | 0 | WOFF (Web Açık [Font](../../aspose.words/font/) Formatı). |
| Ttf | 1 | TTF (TrueType [Font](../../aspose.words/font/) formatı). |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
