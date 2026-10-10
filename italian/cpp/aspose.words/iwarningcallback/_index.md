---
title: "Aspose::Words::IWarningCallback interface"
linktitle: "IWarningCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IWarningCallback interface. Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato per catturare gli avvisi di perdita di fedeltà che possono verificarsi durante il caricamento o il salvataggio del documento in C++."
type: docs
weight: 80000
url: /it/cpp/aspose.words/iwarningcallback/
---
## IWarningCallback interface


Implementa questa interfaccia se desideri avere un tuo metodo personalizzato chiamato per catturare gli avvisi di perdita di fedeltà che possono verificarsi durante il caricamento o il salvataggio del documento.

```cpp
class IWarningCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) | Aspose.Words invoca questo metodo quando incontra qualche problema durante il caricamento o il salvataggio del documento che potrebbe comportare una perdita di formattazione o di fedeltà dei dati. |

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
