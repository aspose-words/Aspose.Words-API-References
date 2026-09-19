---
title: "Metodo Aspose::Words::NodeCollection::IndexOf"
linktitle: "IndexOf"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeCollection::IndexOf. Restituisce l'indice basato su zero del nodo specificato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Restituisce l'indice basato su zero del nodo specificato.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da individuare. |

### ReturnValue

L'indice basato su zero del nodo nella raccolta, se trovato; altrimenti, -1.
## Note


Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a [Count](../get_count/).

## Esempi



Mostra come ottenere l'indice di un nodo in una raccolta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## Vedi anche

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
