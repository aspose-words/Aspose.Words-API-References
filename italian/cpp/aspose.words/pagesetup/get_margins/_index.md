---
title: "Metodo Aspose::Words::PageSetup::get_Margins"
linktitle: "get_Margins"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_Margins. Restituisce o imposta i Margini predefiniti della pagina in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Restituisce o imposta i [Margins](../../margins/) predefiniti della pagina.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## Esempi



Mostra quando ricalcolare il layout della pagina del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Salvare un documento in PDF, in un'immagine o stamparlo per la prima volta lo farà automaticamente
// memorizzare nella cache il layout del documento all'interno delle sue pagine.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifica il documento in qualche modo.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Nella versione corrente di Aspose.Words, la modifica del documento non ricostruisce automaticamente
// il layout della pagina memorizzata nella cache. Se desideriamo che il layout memorizzato nella cache
// per rimanere aggiornato, dovremo aggiornarlo manualmente.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Vedi anche

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
