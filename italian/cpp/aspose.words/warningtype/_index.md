---
title: "Enum Aspose::Words::WarningType"
linktitle: "WarningType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::WarningType. Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento in C++."
type: docs
weight: 129000
url: /it/cpp/aspose.words/warningtype/
---
## WarningType enum


Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento.

```cpp
enum class WarningType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DataLossCategory | 255 | Alcuni testo/carattere/immagine o altri dati mancheranno sia dall'albero del documento dopo il caricamento, sia dal documento creato dopo il salvataggio. |
| DataLoss | 1 | Perdita di dati generica, nessun codice specifico. |
| MajorFormattingLossCategory | 65280 | Il documento risultante o una sua posizione particolare potrebbe apparire sostanzialmente diversa rispetto al documento originale. |
| MajorFormattingLoss | 256 | Perdita di formattazione principale generica, nessun codice specifico. |
| MinorFormattingLossCategory | 16711680 | Il documento risultante o una sua posizione particolare potrebbe apparire leggermente diversa rispetto al documento originale. |
| MinorFormattingLoss | 65536 | Perdita di formattazione minore generica, nessun codice specifico. |
| FontSubstitution | 131072 | [Font](../font/) è stato sostituito. |
| FontEmbedding | 262144 | Perdita delle informazioni dei font incorporati durante il salvataggio del documento. |
| UnexpectedContentCategory | 251658240 | Alcuni contenuti nel documento sorgente non sono stati riconosciuti (cioè non sono supportati), ciò potrebbe o meno causare problemi o provocare perdita di dati/formattazione. |
| UnexpectedContent | 16777216 | Contenuto inaspettato generico, nessun codice specifico. |
| Suggerimento | 268435456 | Avverte di un potenziale problema o suggerisce un miglioramento. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
