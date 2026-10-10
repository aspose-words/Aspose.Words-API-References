---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule Klasse"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule Klasse. Standard-Schriftart-Substitutionsregel. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Standardregel für die Schriftart‑Ersetzung. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Ruft den Standard-Schriftartnamen ab oder legt ihn fest. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Gibt an, ob die Regel aktiviert ist oder nicht. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Setter für [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Setter für [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
