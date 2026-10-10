---
title: "Aspose::Words::FontSubstitutionWarningInfo class"
linktitle: "FontSubstitutionWarningInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FontSubstitutionWarningInfo class. Enthält Informationen über eine Schriftart-Substitutionswarnung, die Aspose.Words beim Laden oder Speichern eines Dokuments in C++ ausgegeben hat."
type: docs
weight: 29500
url: /de/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Enthält Informationen über eine Schriftart‑Ersetzungswarnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Gibt die Beschreibung der Warnung zurück. |
| [get_Reason](./get_reason/)() const | [Font](../font/) Substitutionsgrund. |
| [get_RequestedBold](./get_requestedbold/)() const | Gibt an, ob ein fetter Stil angefordert wurde. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | Angeforderter Schriftfamilienname. |
| [get_RequestedItalic](./get_requesteditalic/)() const | Gibt an, ob ein kursiver Stil angefordert wurde. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Aufgelöste Schriftart. |
| [get_Source](../warninginfo/get_source/)() const | Gibt die Quelle der Warnung zurück. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Gibt den Typ der Warnung zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
