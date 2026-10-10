---
title: "classe Aspose::Words::WarningInfo"
linktitle: "WarningInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::WarningInfo. Contiene informazioni su un avviso che Aspose.Words ha generato durante il caricamento o il salvataggio del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 74000
url: /it/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Contiene informazioni su un avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Description](./get_description/)() const | Restituisce la descrizione dell'avviso. |
| [get_Source](./get_source/)() const | Restituisce la fonte dell'avviso. |
| [get_WarningType](./get_warningtype/)() const | Restituisce il tipo dell'avviso. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


Non si creano istanze di questa classe. Gli oggetti di questa classe sono creati e passati da Aspose.Words al metodo [Warning()](../iwarningcallback/warning/).

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
