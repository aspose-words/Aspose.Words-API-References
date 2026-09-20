---
title: "Aspose::Words::FontSubstitutionReason перечисление"
linktitle: "FontSubstitutionReason"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FontSubstitutionReason перечисление. Указывает причину замены шрифта в C++."
type: docs
weight: 89500
url: /ru/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Указывает причину замены шрифта.

```cpp
enum class FontSubstitutionReason
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) замена альтернативным именем из документа. |
| FontNameSubstitutionRule | 1 | [Font](../font/) замена по правилу имени шрифта. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) замена по правилу конфигурации шрифта. |
| TableSubstitutionRule | 3 | [Font](../font/) замена по правилу таблицы. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) замена по правилу информации о шрифте. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) замена по правилу шрифта по умолчанию. |
| FirstAvailableFont | 6 | [Font](../font/) замена первым доступным шрифтом. |


## Примеры



Показывает, как получить дополнительную информацию о замене шрифта.
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

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
