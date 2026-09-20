---
title: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat"
linktitle: "get_FontFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat. Получает или задаёт ExportFontFormat, используемый для экспорта шрифтов. Значение по умолчанию — Woff в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_fontformat/
---
## HtmlFixedSaveOptions::get_FontFormat method


Получает или задаёт [ExportFontFormat](../../exportfontformat/), используемый для экспорта шрифтов. Значение по умолчанию — [Woff](../../exportfontformat/).

```cpp
Aspose::Words::Saving::ExportFontFormat Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat() const
```


## Примеры



Показывает, как использовать шрифты только с целевой машины при сохранении документа в HTML.
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

## См. также

* Enum [ExportFontFormat](../../exportfontformat/)
* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
