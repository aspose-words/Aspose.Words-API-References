---
title: "Aspose::Words::Document::AcceptAllRevisions metodo"
linktitle: "AcceptAllRevisions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::AcceptAllRevisions metodo. Accetta tutte le modifiche tracciate nel documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Accetta tutte le modifiche tracciate nel documento.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Esempi



Mostra come accettare tutte le modifiche tracciate nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifica il documento mentre tracci le modifiche per creare alcune revisioni.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Possiamo iterare su ogni revisione e accettarla/rifiutarla come parte del nostro documento.
// Se sappiamo di voler accettare ogni revisione, possiamo farlo in modo più diretto chiamando questo metodo.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
