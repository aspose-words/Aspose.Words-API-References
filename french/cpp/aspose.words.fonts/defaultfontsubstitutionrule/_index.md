---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule classe"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule classe. Règle de substitution de police par défaut. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Règle de substitution de police par défaut. Pour en savoir plus, visitez l’article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Obtient ou définit le nom de police par défaut. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Spécifie si la règle est activée ou non. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Définisseur pour [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment définir la règle de substitution de police par défaut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Obtenez la règle de substitution par défaut dans FontSettings.
// Cette règle remplacera toutes les polices manquantes par "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Définissez le substitut de police par défaut sur "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// En utilisant un constructeur de document, ajoutez du texte dans une police que nous ne possédons pas afin de voir la substitution se produire,
// et puis rendez le résultat au format PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Voir aussi

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
