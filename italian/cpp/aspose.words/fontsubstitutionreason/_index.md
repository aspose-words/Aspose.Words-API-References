---
title: "Aspose::Words::FontSubstitutionReason enum"
linktitle: "FontSubstitutionReason"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FontSubstitutionReason enum. Specifica il motivo della sostituzione del carattere in C++."
type: docs
weight: 89500
url: /it/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Specifica il motivo della sostituzione del font.

```cpp
enum class FontSubstitutionReason
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) sostituzione per nome alternativo dal documento. |
| FontNameSubstitutionRule | 1 | [Font](../font/) sostituzione per regola del nome del carattere. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) sostituzione per regola di configurazione del carattere. |
| TableSubstitutionRule | 3 | [Font](../font/) sostituzione per regola di tabella. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) sostituzione tramite regola di informazioni sul font. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) sostituzione tramite regola del font predefinito. |
| FirstAvailableFont | 6 | [Font](../font/) sostituzione con il primo font disponibile. |


## Esempi



Mostra come ottenere informazioni aggiuntive sulla sostituzione del carattere.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
