---
title: "Aspose::Words::FontSubstitutionReason enum"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FontSubstitutionReason enum. Gibt den Grund für die Schriftartsubstitution in C++ an."
type: docs
weight: 89500
url: /de/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Gibt den Grund für die Schriftart-Ersetzung an.

```cpp
enum class FontSubstitutionReason
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) Substitution durch alternativen Namen aus dem Dokument. |
| FontNameSubstitutionRule | 1 | [Font](../font/) Ersetzung nach Schriftartnamen-Regel. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) Ersetzung nach Schriftartkonfigurations-Regel. |
| TableSubstitutionRule | 3 | [Font](../font/) Ersetzung nach Tabellenregel. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) Ersetzung nach Schriftartinfo-Regel. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) Ersetzung nach Standard-Schriftart-Regel. |
| FirstAvailableFont | 6 | [Font](../font/) Ersetzung mit der zuerst verfügbaren Schriftart. |


## Beispiele



Zeigt, wie man zusätzliche Informationen zur Schriftart-Substitution erhält.
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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
