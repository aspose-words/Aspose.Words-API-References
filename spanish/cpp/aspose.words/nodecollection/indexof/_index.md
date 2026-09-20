---
title: "Aspose::Words::NodeCollection::IndexOf método"
linktitle: "IndexOf"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NodeCollection::IndexOf método. Devuelve el índice basado en cero del nodo especificado en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Devuelve el índice basado en cero del nodo especificado.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a localizar. |

### ReturnValue

El índice basado en cero del nodo dentro de la colección, si se encuentra; de lo contrario, -1.
## Observaciones


Este método realiza una búsqueda lineal; por lo tanto, el tiempo medio de ejecución es proporcional a [Count](../get_count/).

## Ejemplos



Muestra cómo obtener el índice de un nodo en una colección.
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

## Ver también

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
