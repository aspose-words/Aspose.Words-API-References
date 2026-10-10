---
title: "Aspose::Words::Saving::ExportFontFormat enum"
linktitle: "ExportFontFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ExportFontFormat enum. Indica il formato utilizzato per esportare i font durante il rendering in formato HTML fisso in C++."
type: docs
weight: 54000
url: /it/cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


Indica il formato utilizzato per esportare i font durante il rendering in formato HTML fisso.

```cpp
enum class ExportFontFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Woff | 0 | WOFF (Formato Web Open [Font](../../aspose.words/font/)). |
| Ttf | 1 | TTF (formato TrueType [Font](../../aspose.words/font/)). |


## Esempi



Mostra come utilizzare solo i font dalla macchina di destinazione durante il salvataggio di un documento in HTML.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
