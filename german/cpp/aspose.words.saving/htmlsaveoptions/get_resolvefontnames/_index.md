---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames Methode"
linktitle: "get_ResolveFontNames"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames Methode. Gibt an, ob Schriftfamiliennamen, die im Dokument verwendet werden, gemäß FontSettings aufgelöst und substituiert werden, wenn sie in HTML-basierte Formate geschrieben werden in C++."
type: docs
weight: 42000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Gibt an, ob Schriftfamiliennamen, die im Dokument verwendet werden, gemäß [FontSettings](../../../aspose.words/document/get_fontsettings/) aufgelöst und substituiert werden, wenn sie in HTML-basierte Formate geschrieben werden.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Hinweise


Standardmäßig ist diese Option auf **false** gesetzt und Schriftfamiliennamen werden in HTML wie in den Quelldokumenten angegeben geschrieben. Das bedeutet, dass [FontSettings](../../../aspose.words/document/get_fontsettings/) ignoriert werden und keine Auflösung oder Substitution von Schriftfamiliennamen durchgeführt wird.

Wenn diese Option auf **true** gesetzt ist, verwendet Aspose.Words [FontSettings](../../../aspose.words/document/get_fontsettings/), um jeden im Quell-Dokument angegebenen Schriftfamiliennamen in den Namen einer verfügbaren Schriftfamilie aufzulösen und bei Bedarf eine Schriftart-Substitution durchzuführen.

## Beispiele



Zeigt, wie alle Schriftarten aufgelöst werden, bevor sie in HTML geschrieben werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Dieses Dokument enthält Text, der eine Schriftart nennt, die wir nicht besitzen.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Wenn wir keine Möglichkeit haben, diese Schriftart zu erhalten, und wir den gesamten Text anzeigen können wollen
// in diesem Dokument in einem Ausgabe-HTML, können wir sie durch eine andere Schriftart ersetzen.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Standardmäßig ist diese Option auf 'False' gesetzt und Aspose.Words schreibt Schriftartnamen wie im Quell-Dokument angegeben.
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
