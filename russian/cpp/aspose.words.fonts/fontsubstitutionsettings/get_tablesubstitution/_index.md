---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution метод"
linktitle: "get_TableSubstitution"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution метод. Параметры, связанные с правилом замены таблицы в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fonts/fontsubstitutionsettings/get_tablesubstitution/
---
## FontSubstitutionSettings::get_TableSubstitution method


[Settings](../../../aspose.words.settings/) related to table substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution() const
```


## Примеры



Показывает, как работать с пользовательскими таблицами замены шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Создайте новое правило замены таблицы и загрузите таблицу замены шрифтов Windows по умолчанию.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Если мы будем выбирать шрифты исключительно из нашей папки, нам понадобится пользовательская таблица замены.
// Мы больше не будем иметь доступа к шрифтам Microsoft Windows,
// например "Arial" или "Times New Roman", так как они не существуют в нашей новой папке шрифтов.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Ниже представлены два способа загрузки таблицы подстановки из файла в локальной файловой системе.
// 1 -  Из потока:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Непосредственно из файла:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Поскольку у нас больше нет доступа к "Arial", наша таблица шрифтов сначала попытается заменить его на "Nonexistent Font".
// У нас нет этого шрифта, поэтому будет использована следующая замена — "Kreon", найденный в папке "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Мы можем расширить эту таблицу программно. Мы добавим запись, заменяющую "Times New Roman" на "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Мы можем добавить вторичную резервную замену для существующей записи шрифта с помощью AddSubstitutes().
// Если "Arvo" недоступен, наша таблица будет искать "M+ 2m" как второй вариант замены.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() может установить новый список заменяющих шрифтов для шрифта.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Запись текста шрифтами, к которым у нас нет доступа, вызовет наши правила подстановки.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## См. также

* Class [TableSubstitutionRule](../../tablesubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
