---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics"
linktitle: "get_KeepOriginalFontMetrics"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics. Ottiene o imposta un'indicazione se le metriche originali del font devono essere utilizzate dopo la sostituzione del font. Il valore predefinito è true in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.layout/layoutoptions/get_keeporiginalfontmetrics/
---
## LayoutOptions::get_KeepOriginalFontMetrics method


Ottiene o imposta un'indicazione se le metriche originali del carattere devono essere utilizzate dopo la sostituzione del carattere. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics() const
```


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

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
