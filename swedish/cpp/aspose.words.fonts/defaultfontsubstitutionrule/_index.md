---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule-klass"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule-klass. Standardregel för teckensnittssubstitution. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Standardregel för teckensnittssubstitution. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Hämtar eller anger standardteckensnittets namn. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Anger om regeln är aktiverad eller inte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Sättare för [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Sättare för [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man ställer in standardteckensnittsbytesregeln.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Hämta standardbytesregeln i FontSettings.
// Denna regel kommer att ersätta alla saknade teckensnitt med "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Ställ in standardteckensnittsbyte till "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Med en dokumentbyggare, lägg till lite text i ett teckensnitt som vi inte har för att se ersättningen ske,
// och rendera sedan resultatet i en PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Se även

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
