---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metod"
linktitle: "get_DefaultFontSubstitution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metod. Inställningar relaterade till standardteckensnittssubstitutionsregeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


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

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
