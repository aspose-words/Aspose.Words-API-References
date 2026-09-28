---
title: "Класс Aspose::Words::FontSubstitutionWarningInfo"
linktitle: "FontSubstitutionWarningInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FontSubstitutionWarningInfo класс. Содержит информацию о предупреждении о замене шрифта, которое Aspose.Words выдал во время загрузки или сохранения документа в C++."
type: docs
weight: 29500
url: /ru/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Содержит информацию о предупреждении о замене шрифта, которое Aspose.Words выдал при загрузке или сохранении документа.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Возвращает описание предупреждения. |
| [get_Reason](./get_reason/)() const | [Font](../font/) причина замены шрифта. |
| [get_RequestedBold](./get_requestedbold/)() const | Указывает, был ли запрошен полужирный стиль. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | Запрошенное название семейства шрифтов. |
| [get_RequestedItalic](./get_requesteditalic/)() const | Указывает, был ли запрошен курсивный стиль. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Разрешённый шрифт. |
| [get_Source](../warninginfo/get_source/)() const | Возвращает источник предупреждения. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Возвращает тип предупреждения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
