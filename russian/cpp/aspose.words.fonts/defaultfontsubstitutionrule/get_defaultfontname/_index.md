---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName метод"
linktitle: "get_DefaultFontName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName метод. Получает или задает имя шрифта по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


Получает или задает имя шрифта по умолчанию.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## Примечания


Значение по умолчанию — 'Times New Roman'.

## Примеры



Показывает, как указать шрифт по умолчанию.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Источники шрифтов, используемые документом, содержат шрифт \"Arial\", но не \"Arvo\".
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Установите свойство \"DefaultFontName\" в значение \"Courier New\", чтобы
// при рендеринге документа применять этот шрифт во всех случаях, когда другой шрифт недоступен.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Aspose.Words теперь будет использовать шрифт по умолчанию вместо любых отсутствующих шрифтов при любых вызовах рендеринга.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


Показывает, как установить правило замены шрифтов по умолчанию.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Получите правило замены по умолчанию в FontSettings.
// Это правило заменит все отсутствующие шрифты на "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Установите замену шрифта по умолчанию на "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Используя DocumentBuilder, добавьте некоторый текст шрифтом, которого у нас нет, чтобы увидеть замену,
// а затем отрендерите результат в PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## См. также

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
