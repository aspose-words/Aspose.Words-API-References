---
title: "Aspose::Words::FontSubstitutionWarningInfo class"
linktitle: "FontSubstitutionWarningInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FontSubstitutionWarningInfo class. Innehåller information om en varning för teckensnittssubstitution som Aspose.Words utfärdade under dokumentladdning eller -sparande i C++."
type: docs
weight: 29500
url: /sv/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Innehåller information om en teckensnittsersättningsvarning som Aspose.Words gav under inläsning eller sparande av dokument.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Returnerar beskrivningen av varningen. |
| [get_Reason](./get_reason/)() const | [Font](../font/) orsak till substitution. |
| [get_RequestedBold](./get_requestedbold/)() const | Indikerar om fet stil begärdes. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | Begärt teckensnittsfamiljenamn. |
| [get_RequestedItalic](./get_requesteditalic/)() const | Indikerar om kursiv stil begärdes. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Upplöst teckensnitt. |
| [get_Source](../warninginfo/get_source/)() const | Returnerar källan till varningen. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Returnerar varningens typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får ytterligare information om teckensnittssubstitution.
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

## Se även

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
