---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings class. Указывает настройки механизма подстановки шрифтов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Указывает настройки механизма подстановки шрифтов. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionSettings : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) связанные с правилом подстановки шрифта по умолчанию. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) связанные с правилом подстановки конфигурации шрифта. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) связанные с правилом подстановки информации о шрифте. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) связанные с правилом подстановки имени шрифта. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) связанные с правилом подстановки таблицы. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

Порядок правил следующий:1. [Font](../../aspose.words/font/) правило подстановки имени (включено по умолчанию)
1. [Font](../../aspose.words/font/) правило подстановки конфигурации (отключено по умолчанию)
1. Правило подстановки таблицы (включено по умолчанию)
1. [Font](../../aspose.words/font/) правило подстановки информации (включено по умолчанию)
1. Правило шрифта по умолчанию (включено по умолчанию)



Обратите внимание, что правило подстановки информации о шрифте всегда будет определять шрифт, если доступен [FontInfo](../fontinfo/), и переопределит правило шрифта по умолчанию. Если вы хотите использовать правило шрифта по умолчанию, то следует отключить правило подстановки информации о шрифте.

Обратите внимание, что правило подстановки конфигурации шрифта будет определять шрифт в большинстве случаев и, следовательно, переопределяет все остальные правила.

## Примеры



Показывает, как получить доступ к системному источнику шрифтов документа и задать замену шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// По умолчанию пустой документ всегда содержит системный источник шрифтов.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Установите шрифт, который существует в каталоге Windows Fonts, в качестве замены для отсутствующего шрифта.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// В качестве альтернативы мы можем добавить папочный источник шрифтов, в котором соответствующая папка содержит шрифт.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Сброс источников шрифтов всё равно оставляет у нас системный источник шрифтов, а также наши замены.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
