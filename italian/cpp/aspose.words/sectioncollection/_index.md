---
title: "Aspose::Words::SectionCollection classe"
linktitle: "SectionCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SectionCollection class. Una raccolta di oggetti Section nel documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 59000
url: /it/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Una raccolta di oggetti [Section](../section/) nel documento. Per saperne di più, visita l'articolo della documentazione [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Aggiunge un nodo alla fine della collezione. |
| [Clear](../nodecollection/clear/)() | Rimuove tutti i nodi da questa collezione e dal documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina se un nodo è nella collezione. |
| [get_Count](../nodecollection/get_count/)() | Ottiene il numero di nodi nella collezione. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fornisce una semplice iterazione in stile "foreach" sulla collezione di nodi. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera una sezione all'indice specificato. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](./toarray/)() | Copia tutte le sezioni dalla raccolta in un nuovo array di sezioni. |
| static [Type](./type/)() |  |
## Note


Un documento Microsoft Word può contenere più sezioni. Per creare una sezione in Microsoft Word, seleziona il comando Inserisci/Interruzione e scegli un tipo di interruzione. L'interruzione specifica se la sezione inizia su una nuova pagina o sulla stessa pagina.

L'inserimento e la rimozione programmati di sezioni possono essere usati per personalizzare i documenti prodotti durante l'unione di stampa. Se un documento deve contenere contenuti diversi o parti del contenuto a seconda di alcuni criteri, è possibile creare un documento "master" che contiene più sezioni e cancellare alcune delle sezioni prima o dopo l'unione di stampa.

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
