---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet metodo"
linktitle: "get_SheetsPerBooklet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet metodo. Restituisce o imposta il numero di pagine da includere in ogni opuscolo in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Restituisce o imposta il numero di pagine da includere in ogni opuscolo.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Esempi



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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
