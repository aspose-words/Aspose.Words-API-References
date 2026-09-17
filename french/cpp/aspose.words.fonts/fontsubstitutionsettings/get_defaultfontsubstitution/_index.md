---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution méthode"
linktitle: "get_DefaultFontSubstitution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution méthode. Paramètres liés à la règle de substitution de police par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


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

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
