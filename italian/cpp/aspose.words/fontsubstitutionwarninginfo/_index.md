---
title: "Classe Aspose::Words::FontSubstitutionWarningInfo"
linktitle: "FontSubstitutionWarningInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::FontSubstitutionWarningInfo. Contiene informazioni su un avviso di sostituzione del carattere emesso da Aspose.Words durante il caricamento o il salvataggio del documento in C++."
type: docs
weight: 29500
url: /it/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Contiene informazioni su un avviso di sostituzione del carattere che Aspose.Words ha emesso durante il caricamento o il salvataggio del documento.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Restituisce la descrizione dell'avviso. |
| [get_Reason](./get_reason/)() const | Motivo della sostituzione del [Font](../font/). |
| [get_RequestedBold](./get_requestedbold/)() const | Indica se è stato richiesto lo stile grassetto. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | Nome della famiglia di caratteri richiesto. |
| [get_RequestedItalic](./get_requesteditalic/)() const | Indica se è stato richiesto lo stile corsivo. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Carattere risolto. |
| [get_Source](../warninginfo/get_source/)() const | Restituisce la fonte dell'avviso. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Restituisce il tipo dell'avviso. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
