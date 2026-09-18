---
title: "Aspose::Words::Saving::ExportFontFormat enum"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ExportFontFormat enum. Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format in C++ verwendet wird."
type: docs
weight: 54000
url: /de/cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format verwendet wird.

```cpp
enum class ExportFontFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Woff | 0 | WOFF (Web Open [Font](../../aspose.words/font/) Format). |
| Ttf | 1 | TTF (TrueType [Font](../../aspose.words/font/) Format). |


## Beispiele



Zeigt, wie man Schriftarten nur vom Zielrechner verwendet, wenn man ein Dokument als HTML speichert.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
