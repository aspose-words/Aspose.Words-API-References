---
title: "Metodo Aspose::Words::PageSetup::get_MultiplePages"
linktitle: "get_MultiplePages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_MultiplePages. Per documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come un libretto in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo.

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
```


## Esempi



Mostra come impostare i margini di rilegatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci testo che si estende su più pagine.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Una rilegatura aggiunge spazi bianchi sia al margine sinistro che a quello destro della pagina,
// che compensa la piegatura centrale delle pagine in un libro che invade il layout della pagina.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Determina quanto spazio hanno le nostre pagine per il testo all'interno dei margini e poi aggiungi una quantità per imbottire un margine.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Imposta la proprietà "RtlGutter" su "true" per posizionare la rilegatura in una posizione più adatta per il testo da destra a sinistra.
pageSetup->set_RtlGutter(true);

// Imposta la proprietà "MultiplePages" su "MultiplePagesType.MirrorMargins" per alternare
// la posizione laterale sinistra/destra dei margini di ogni pagina.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


Mostra come configurare un documento che può essere stampato come piegatura a libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci testo che si estende su 16 pagine.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configura la proprietà "PageSetup" della prima sezione per stampare il documento nella forma di una piegatura a libro.
// Quando stampiamo questo documento su entrambi i lati, possiamo prendere le pagine per impilarle
// e piegarle tutte a metà contemporaneamente. Il contenuto del documento si allineerà in una piegatura a libro.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Possiamo specificare il numero di fogli solo in multipli di 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Vedi anche

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
