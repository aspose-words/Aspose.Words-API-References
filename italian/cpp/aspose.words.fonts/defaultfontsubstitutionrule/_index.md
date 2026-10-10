---
title: "Classe Aspose::Words::Fonts::DefaultFontSubstitutionRule"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fonts::DefaultFontSubstitutionRule. Regola di sostituzione del carattere predefinito. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Regola predefinita di sostituzione dei caratteri. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Ottiene o imposta il nome del carattere predefinito. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifica se la regola è abilitata o meno. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Impostatore per [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Impostatore per [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
