---
title: "Aspose::Words::PageSetup::get_Bidi metodo"
linktitle: "get_Bidi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_Bidi metodo. Specifica che questa sezione contiene testo bidirezionale (script complessi) in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Specifica che questa sezione contiene testo bidirezionale (script complessi).

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Note


Quando **true**, le colonne in questa sezione sono disposte da destra a sinistra.

## Esempi



Mostra come impostare l'ordine delle colonne di testo in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Imposta la proprietà "Bidi" su "true" per disporre le colonne a partire dal lato destro della pagina.
// L'ordine delle colonne corrisponderà alla direzione del testo da destra a sinistra.
// Imposta la proprietà "Bidi" su "false" per disporre le colonne a partire dal lato sinistro della pagina.
// L'ordine delle colonne corrisponderà alla direzione del testo da sinistra a destra.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
