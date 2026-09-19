---
title: "Aspose::Words::Document::UpdatePageLayout method"
linktitle: "UpdatePageLayout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::UpdatePageLayout method. Ricostruisce il layout di pagina del documento in C++."
type: docs
weight: 98000
url: /it/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Ricostruisce il layout di pagina del documento.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Note


Questo metodo formatta un documento in pagine e aggiorna i campi relativi ai numeri di pagina nel documento, come PAGE, PAGES, PAGEREF e REF. Le informazioni aggiornate sul layout di pagina sono necessarie per una corretta resa del documento in formati a pagina fissa.

Questo metodo viene invocato automaticamente quando si converte per la prima volta un documento in PDF, XPS, immagine o lo si stampa. Tuttavia, se si modifica il documento dopo il rendering e si tenta di renderizzarlo nuovamente, Aspose.Words non aggiornerà automaticamente il layout di pagina. In questo caso è necessario chiamare [UpdatePageLayout](./) prima di renderizzare nuovamente.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
