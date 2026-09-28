---
title: "Aspose::Words::Saving::ExportFontFormat enum"
linktitle: "ExportFontFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ExportFontFormat enum. Указывает формат, используемый для экспорта шрифтов при рендеринге в фиксированный формат HTML на C++."
type: docs
weight: 54000
url: /ru/cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


Указывает формат, используемый для экспорта шрифтов при рендеринге в фиксированный формат HTML.

```cpp
enum class ExportFontFormat
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Woff | 0 | WOFF (Web Open [Font](../../aspose.words/font/) Format). |
| Ttf | 1 | TTF (TrueType [Font](../../aspose.words/font/) формат). |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
