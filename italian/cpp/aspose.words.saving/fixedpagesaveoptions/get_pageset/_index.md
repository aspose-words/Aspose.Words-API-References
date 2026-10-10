---
title: "Metodo Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet"
linktitle: "get_PageSet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet. Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


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

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
