---
title: "Metodo Aspose::Words::Document::UpdateWordCount"
linktitle: "UpdateWordCount"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::UpdateWordCount. Aggiorna le proprietà del conteggio parole del documento in C++."
type: docs
weight: 101000
url: /it/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Aggiorna le proprietà del conteggio parole del documento.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Note


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Nota che [UpdateWordCount](./) non aggiorna le proprietà del numero di righe e pagine. Usa la sovraccarico di [UpdateWordCount](./) e passa il valore **true** come parametro per farlo.

Quando utilizzi una versione di valutazione, la filigrana di valutazione verrà inclusa anche nel conteggio parole.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Aggiorna le proprietà del conteggio parole del documento, aggiornando facoltativamente la proprietà [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/).

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| updateLinesCount | bool | **true** se il numero di righe nel documento deve essere calcolato. |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
