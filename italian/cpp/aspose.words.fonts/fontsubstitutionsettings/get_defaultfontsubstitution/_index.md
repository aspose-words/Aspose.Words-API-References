---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metodo"
linktitle: "get_DefaultFontSubstitution"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metodo. Impostazioni relative alla regola di sostituzione del font predefinito in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


## Esempi



Mostra come impostare la regola di sostituzione del carattere predefinito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Ottieni la regola di sostituzione predefinita all'interno di FontSettings.
// Questa regola sostituirà tutti i caratteri mancanti con "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Imposta il sostituto di carattere predefinito su "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Utilizzando un document builder, aggiungi del testo in un carattere che non possediamo per vedere avvenire la sostituzione,
// e poi renderizza il risultato in un PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Vedi anche

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
