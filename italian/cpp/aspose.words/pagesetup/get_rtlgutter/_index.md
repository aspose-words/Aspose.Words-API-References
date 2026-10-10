---
title: "Aspose::Words::PageSetup::get_RtlGutter metodo"
linktitle: "get_RtlGutter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_RtlGutter method. Ottiene o imposta se Microsoft Word utilizza i margini laterali per la sezione in base a una lingua da destra a sinistra o da sinistra a destra in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Ottiene o imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
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

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
