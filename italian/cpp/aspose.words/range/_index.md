---
title: "classe Aspose::Words::Range"
linktitle: "Intervallo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Range. Rappresenta un'area contigua in un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 51000
url: /it/cpp/aspose.words/range/
---
## Range class


Rappresenta un'area contigua in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Delete](./delete/)() | Elimina tutti i caratteri dell'intervallo. |
| [get_Bookmarks](./get_bookmarks/)() | Restituisce una collezione di [Bookmarks](./get_bookmarks/) che rappresenta tutti i segnalibri nell'intervallo. |
| [get_Fields](./get_fields/)() | Restituisce una collezione di [Fields](./get_fields/) che rappresenta tutti i campi nell'intervallo. |
| [get_FormFields](./get_formfields/)() | Restituisce una collezione di [FormFields](./get_formfields/) che rappresenta tutti i campi modulo nell'intervallo. |
| [get_Revisions](./get_revisions/)() | Ottiene una collezione di revisioni (modifiche tracciate) presenti in questo intervallo. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Restituisce una collezione di [StructuredDocumentTags](./get_structureddocumenttags/) che rappresenta tutti i tag di documento strutturato nell'intervallo. |
| [get_Text](./get_text/)() | Ottiene il testo dell'intervallo. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Modifica i valori del tipo di campo [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) di [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) e [FieldEnd](../../aspose.words.fields/fieldend/) in questo intervallo affinché corrispondano ai tipi di campo contenuti nei codici dei campi. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Sostituisce tutte le occorrenze di un modello di caratteri specificato da un'espressione regolare con un'altra stringa. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Sostituisce tutte le occorrenze di un modello di caratteri specificato da un'espressione regolare con un'altra stringa. |
| [ToDocument](./todocument/)() | Costruisce un nuovo documento completo che contiene l'intervallo. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Scollega i campi in questo intervallo. |
| [UpdateFields](./updatefields/)() | Aggiorna i valori dei campi del documento in questo intervallo. |
## Note


Il documento è rappresentato da un albero di nodi e i nodi forniscono operazioni per lavorare con l'albero, ma alcune operazioni sono più facili da eseguire se il documento è trattato come una sequenza contigua di testo.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Esempi



Mostra come ottenere il contenuto testuale di tutti i nodi coperti da un intervallo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
