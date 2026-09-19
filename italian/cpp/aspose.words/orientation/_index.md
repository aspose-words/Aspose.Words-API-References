---
title: "Aspose::Words::Orientation enum"
linktitle: "Orientamento"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Orientation enum. Specifica l'orientamento della pagina in C++."
type: docs
weight: 104000
url: /it/cpp/aspose.words/orientation/
---
## Orientation enum


Specifica l'orientamento della pagina.

```cpp
enum class Orientation
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Verticale | 1 | Orientamento di pagina verticale (stretto e alto). |
| Orizzontale | 2 | Orientamento di pagina orizzontale (ampio e corto). |


## Esempi



Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifica le proprietà di configurazione della pagina per la sezione corrente del builder e aggiungi testo.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Se avviamo una nuova sezione utilizzando un document builder,
// eredità le proprietà di configurazione della pagina correnti del builder.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Possiamo ripristinare le sue proprietà di configurazione della pagina ai valori predefiniti usando il metodo "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
