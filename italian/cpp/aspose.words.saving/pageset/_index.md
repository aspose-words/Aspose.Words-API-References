---
title: "Classe Aspose::Words::Saving::PageSet"
linktitle: "PageSet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Saving::PageSet. Descrive un insieme casuale di pagine. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.saving/pageset/
---
## PageSet class


Descrive un insieme casuale di pagine. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [get_All](./get_all/)() | Restituisce un insieme con tutte le pagine del documento nel loro ordine originale. |
| static [get_Even](./get_even/)() | Restituisce un insieme con tutte le pagine pari del documento nel loro ordine originale. |
| static [get_Odd](./get_odd/)() | Restituisce un insieme con tutte le pagine dispari del documento nel loro ordine originale. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Crea un insieme di una sola pagina basato su un indice di pagina esatto. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Crea un insieme di pagine basato su indici di pagina esatti. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Crea un insieme di pagine basato su intervalli. |
| static [Type](./type/)() |  |

## Esempi



Mostra come rendere una pagina da un documento in un'immagine JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Imposta "PageSet" a "1" per selezionare la seconda pagina tramite
// l'indice basato su zero da cui iniziare a rendere il documento.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Quando salviamo il documento nel formato JPEG, Aspose.Words rende solo una pagina.
// Questa immagine conterrà una pagina a partire dalla pagina due,
// che sarà semplicemente la seconda pagina del documento originale.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
