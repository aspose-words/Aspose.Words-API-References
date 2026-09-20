---
title: "Метод Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes"
linktitle: "SetSubstitutes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes. Переопределите имена заменяющих шрифтов для заданного оригинального имени шрифта в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Переопределяет имена заменяющих шрифтов для указанного оригинального имени шрифта.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| originalFontName | const System::String\& | Исходное имя шрифта. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Список альтернативных имен шрифтов. |

## Примеры



Показывает, как задать правила замены шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Источник шрифтов по умолчанию содержит первый шрифт, используемый в документе.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Второй шрифт, \"Amethysta\", недоступен.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Мы можем настроить таблицу замены шрифтов, которая определяет
// какие шрифты Aspose.Words будет использовать в качестве замен для недоступных шрифтов.
// Установите два заменяющих шрифта для \"Amethysta\": \"Arvo\" и \"Courier New\".
// Если первый заменяющий шрифт недоступен, Aspose.Words пытается использовать второй заменяющий шрифт и так далее.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// \"Amethysta\" недоступен, и правило замены указывает, что первым шрифтом‑заменой будет \"Arvo\".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// \"Arvo\" также недоступен, но \"Courier New\" доступен.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Выходной документ отобразит текст, использующий шрифт \"Amethysta\", отформатированный шрифтом \"Courier New\".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
