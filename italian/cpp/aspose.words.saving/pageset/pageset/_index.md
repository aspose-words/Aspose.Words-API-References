---
title: "Costruttore Aspose::Words::Saving::PageSet::PageSet"
linktitle: "PageSet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Saving::PageSet::PageSet. Crea un insieme di pagine basato su indici di pagina esatti in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Crea un insieme di pagine basato su indici di pagina esatti.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pagine | const System::ArrayPtr\<int32_t\>\& | Indici delle pagine basati su zero. |

## Esempi



Mostra come estrarre le pagine basandosi su indici di pagina esatti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi cinque pagine al documento.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Crea un oggetto "XpsSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare come quel metodo converte il documento in .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Usa la proprietà "PageSet" per selezionare un insieme di pagine del documento da salvare nell'output XPS.
// In questo caso, sceglieremo, tramite un indice basato su zero, solo tre pagine: pagina 1, pagina 2 e pagina 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Vedi anche

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Crea un insieme di pagine basato su intervalli.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| intervalli | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Array di intervalli di pagine. |

## Esempi



Mostra come estrarre pagine basate su intervalli di pagine esatti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Vedi anche

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Crea un insieme di una sola pagina basato su un indice di pagina esatto.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pagina | int32_t | Indice della pagina basato su zero. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
