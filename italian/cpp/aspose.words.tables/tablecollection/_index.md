---
title: "Aspose::Words::Tables::TableCollection class"
linktitle: "TableCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::TableCollection class. Fornisce accesso tipizzato a una raccolta di nodi Table. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Fornisce accesso tipizzato a una raccolta di nodi [Table](../table/). Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Recupera un [Table](../table/) all'indice specificato. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](./toarray/)() | Copia tutte le tabelle dalla raccolta in un nuovo array di tabelle. |
| static [Type](./type/)() |  |

## Esempi



Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

## Vedi anche

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
