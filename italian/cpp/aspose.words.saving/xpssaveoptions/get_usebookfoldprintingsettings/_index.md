---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metodo"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metodo. Ottiene o imposta un valore booleano che indica se il documento deve essere salvato usando un layout di stampa a libretto, se è specificato tramite MultiplePages in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Ottiene o imposta un valore booleano che indica se il documento deve essere salvato usando un layout di stampa a libretto, se è specificato tramite [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Note


Se questa opzione è specificata, [PageSet](../../fixedpagesaveoptions/get_pageset/) viene ignorato durante il salvataggio. Questo comportamento corrisponde a MS Word. Se le impostazioni di stampa a libretto non sono specificate nella configurazione della pagina, questa opzione non avrà alcun effetto.

## Esempi



Mostra come salvare un documento nel formato XPS sotto forma di piega libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Crea un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare come quel metodo converte il documento in .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare i contenuti
// nell'output XPS in modo da aiutarci a usarlo per creare un opuscolo.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "false" per rendere l'XPS normalmente.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Se stiamo rendendo il documento come libretto, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di configurazione pagina di tutte le sezioni a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Una volta stampato questo documento, possiamo trasformarlo in un opuscolo impilando le pagine
// per uscire dalla stampante e piegare a metà.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Vedi anche

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
