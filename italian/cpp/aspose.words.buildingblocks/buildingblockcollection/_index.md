---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection classe"
linktitle: "BuildingBlockCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection classe. Una raccolta di oggetti BuildingBlock nel documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


Una raccolta di oggetti [BuildingBlock](../buildingblock/) nel documento. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Aggiunge un nodo alla fine della collezione. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa collezione e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina se un nodo è nella collezione. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Ottiene il numero di nodi nella collezione. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Fornisce una semplice iterazione in stile "foreach" sulla collezione di nodi. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un blocco di costruzione all'indice specificato. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](./toarray/)() | Copia tutti i blocchi di costruzione dalla raccolta in un nuovo array di blocchi di costruzione. |
| static [Type](./type/)() |  |
## Note


Non si creano istanze di questa classe direttamente. Per accedere a una raccolta di blocchi di costruzione utilizza la proprietà [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## Vedi anche

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
