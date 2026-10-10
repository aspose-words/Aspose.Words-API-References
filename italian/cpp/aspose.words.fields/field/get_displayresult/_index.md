---
title: "Aspose::Words::Fields::Field::get_DisplayResult method"
linktitle: "get_DisplayResult"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::get_DisplayResult method. Ottiene il testo che rappresenta il risultato visualizzato del campo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Restituisce il testo che rappresenta il risultato del campo visualizzato.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Esempi



Mostra come ottenere il testo reale che un campo visualizza nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Possiamo usare la proprietà DisplayResult per verificare quale testo esatto
// un campo visualizzerebbe al suo posto nel documento.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// I campi non mantengono valori di risultato accurati in tempo reale.
// Per assicurarci che i nostri campi visualizzino risultati accurati in qualsiasi momento,
// come subito prima di un'operazione di salvataggio, dobbiamo aggiornarli manualmente.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
