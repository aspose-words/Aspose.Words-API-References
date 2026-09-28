---
title: "Класс Aspose::Words::Fonts::DefaultFontSubstitutionRule"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Fonts::DefaultFontSubstitutionRule. Правило замены шрифтов по умолчанию. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Правило замены шрифта по умолчанию. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Получает или задает имя шрифта по умолчанию. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Указывает, включено правило или нет. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Сеттер для [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Сеттер для [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

## Примеры



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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
