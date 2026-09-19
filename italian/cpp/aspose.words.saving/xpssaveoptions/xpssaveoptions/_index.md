---
title: "Costruttore Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions"
linktitle: "XpsSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions. Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato Xps in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Esempi



Mostra come limitare il livello dei titoli che appariranno nella struttura di un documento XPS salvato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci titoli che possono servire come voci di indice a livelli 1, 2 e poi 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Crea un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare come quel metodo converte il documento in .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Il documento XPS di output conterrà una struttura, un indice che elenca i titoli nel corpo del documento.
// Facendo clic su una voce di questa struttura si verrà portati alla posizione del relativo titolo.
// Imposta la proprietà "HeadingsOutlineLevels" a "2" per escludere tutti i titoli il cui livello è superiore a 2 dalla struttura.
// Gli ultimi due titoli inseriti sopra non appariranno.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Vedi anche

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nei formati [Xps](../../../aspose.words/saveformat/) o [OpenXps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
