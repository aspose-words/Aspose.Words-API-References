---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution Methode"
linktitle: "get_DefaultFontSubstitution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution Methode. Einstellungen, die mit der Standard-Schriftart-Substitutionsregel in C++ zusammenhängen."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


## Beispiele



Zeigt, wie man die Standard-Schriftart-Substitutionsregel festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Rufen Sie die Standard-Substitutionsregel innerhalb von FontSettings ab.
// Diese Regel ersetzt alle fehlenden Schriften durch "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Setzen Sie die Standard-Schriftart-Substitution auf "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Verwenden Sie einen Document Builder, fügen Sie Text in einer Schriftart hinzu, die wir nicht haben, um die Substitution zu sehen,
// und rendern Sie anschließend das Ergebnis in ein PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Siehe auch

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
