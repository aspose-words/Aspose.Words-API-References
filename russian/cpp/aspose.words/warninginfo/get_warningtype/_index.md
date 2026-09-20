---
title: "Aspose::Words::WarningInfo::get_WarningType метод"
linktitle: "get_WarningType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WarningInfo::get_WarningType метод. Возвращает тип предупреждения в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/warninginfo/get_warningtype/
---
## WarningInfo::get_WarningType method


Возвращает тип предупреждения.

```cpp
Aspose::Words::WarningType Aspose::Words::WarningInfo::get_WarningType() const
```


## Примеры



Показывает, как установить свойство для поиска наиболее подходящего шрифта при отсутствии нужного шрифта среди доступных источников шрифтов.
```cpp
// Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Назначьте обратный вызов для обработки предупреждений о замене шрифтов.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Установите имя шрифта по умолчанию и включите замену шрифтов.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// После замены шрифтов следует использовать исходные метрики шрифта.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```


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

* Enum [WarningType](../../warningtype/)
* Class [WarningInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
