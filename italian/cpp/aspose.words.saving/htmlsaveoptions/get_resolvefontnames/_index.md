---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames metodo"
linktitle: "get_ResolveFontNames"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames metodo. Specifica se i nomi delle famiglie di caratteri usati nel documento vengono risolti e sostituiti secondo FontSettings quando vengono scritti in formati basati su HTML in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Specifica se i nomi delle famiglie di caratteri usati nel documento vengono risolti e sostituiti secondo [FontSettings](../../../aspose.words/document/get_fontsettings/) quando vengono scritti in formati basati su HTML.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Note


Per impostazione predefinita, questa opzione è impostata su **false** e i nomi delle famiglie di caratteri vengono scritti in HTML come specificato nei documenti di origine. Cioè, [FontSettings](../../../aspose.words/document/get_fontsettings/) sono ignorati e non viene eseguita alcuna risoluzione o sostituzione dei nomi delle famiglie di caratteri.

Se questa opzione è impostata su **true**, Aspose.Words utilizza [FontSettings](../../../aspose.words/document/get_fontsettings/) per risolvere ogni nome di famiglia di caratteri specificato in un documento di origine nel nome di una famiglia di caratteri disponibile, eseguendo la sostituzione dei caratteri secondo necessità.

## Esempi



Mostra come risolvere tutti i nomi dei caratteri prima di scriverli in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Questo documento contiene testo che cita un carattere che non possediamo.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Se non abbiamo modo di ottenere questo carattere e vogliamo poter visualizzare tutto il testo
// in questo documento in un HTML di output, possiamo sostituirlo con un altro carattere.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Per impostazione predefinita, questa opzione è impostata su 'False' e Aspose.Words scrive i nomi dei caratteri come specificato nel documento di origine
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
