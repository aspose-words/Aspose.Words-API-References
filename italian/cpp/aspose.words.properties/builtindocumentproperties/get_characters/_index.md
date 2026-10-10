---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters metodo"
linktitle: "get_Characters"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters metodo. Rappresenta una stima del numero di caratteri nel documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_characters/
---
## BuiltInDocumentProperties::get_Characters method


Rappresenta una stima del numero di caratteri nel documento.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters()
```

## Note


Aspose.Words aggiorna questa proprietà quando chiami [UpdateWordCount](../../../aspose.words/document/updatewordcount/).

## Esempi



Mostra come aggiornare tutte le etichette delle liste in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words non traccia metriche del documento come queste in tempo reale.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Per ottenere valori accurati per tre di queste proprietà, dovremo aggiornarle manualmente.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Per il conteggio delle righe, dovremo chiamare una sovraccarico specifica del metodo di aggiornamento.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
