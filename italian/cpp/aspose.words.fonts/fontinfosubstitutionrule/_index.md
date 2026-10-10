---
title: "Aspose::Words::Fonts::FontInfoSubstitutionRule class"
linktitle: "FontInfoSubstitutionRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfoSubstitutionRule class. Regola di sostituzione delle informazioni del carattere. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class


[Font](../../aspose.words/font/) info substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifica se la regola è abilitata o meno. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Impostatore per [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un carattere mancante tra le sorgenti di caratteri disponibili.
```cpp
// Apri un documento che contiene testo formattato con un carattere che non esiste in nessuna delle nostre sorgenti di caratteri.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Assegna una callback per gestire gli avvisi di sostituzione dei caratteri.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Imposta un nome di carattere predefinito e abilita la sostituzione dei caratteri.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Le metriche originali del carattere dovrebbero essere usate dopo la sostituzione del carattere.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Riceveremo un avviso di sostituzione del carattere se salviamo un documento con un carattere mancante.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Vedi anche

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
