---
title: "Metodo Aspose::Words::NodeCollection::RemoveAt"
linktitle: "RemoveAt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeCollection::RemoveAt. Rimuove il nodo all'indice specificato dalla collezione e dal documento in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Rimuove il nodo all'indice specificato dalla raccolta e dal documento.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero del nodo. Sono consentiti indici negativi e indicano l'accesso dalla fine dell'elenco. Ad esempio, -1 indica l'ultimo nodo, -2 il penultimo e così via. |

## Esempi



Mostra come aggiungere e rimuovere sezioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimina la prima sezione dal documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Aggiungi una copia di quella che è ora la prima sezione alla fine del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Vedi anche

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
