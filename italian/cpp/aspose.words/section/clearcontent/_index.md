---
title: "Aspose::Words::Section::ClearContent metodo"
linktitle: "ClearContent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::ClearContent metodo. Cancella la sezione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Cancella la sezione.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Note


Il testo di [Body](../get_body/) viene cancellato, rimane un solo paragrafo vuoto che rappresenta l'interruzione di sezione.

Il testo di tutte le intestazioni e i piè di pagina viene cancellato, ma gli oggetti [HeaderFooter](../../headerfooter/) stessi non vengono rimossi.

## Esempi



Mostra come cancellare il contenuto di una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Eseguire il metodo \"ClearContent\" rimuoverà tutti i contenuti della sezione
// ma lascerà un paragrafo vuoto per aggiungere nuovamente contenuto.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Vedi anche

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
