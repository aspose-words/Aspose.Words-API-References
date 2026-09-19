---
title: "Costruttore PageRange di Aspose::Words::Saving::PageRange"
linktitle: "PageRange"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore PageRange di Aspose::Words::Saving::PageRange. Crea un nuovo oggetto intervallo di pagine in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Crea un nuovo oggetto intervallo di pagine.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| da | int32_t | L'indice della pagina iniziale basato su zero. |
| a | int32_t | L'indice della pagina finale basato su zero. Se supera l'indice dell'ultima pagina del documento, viene troncato per adattarsi al documento durante il rendering. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
