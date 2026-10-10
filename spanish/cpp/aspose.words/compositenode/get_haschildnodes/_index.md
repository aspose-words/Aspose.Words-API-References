---
title: "Método Aspose::Words::CompositeNode::get_HasChildNodes"
linktitle: "get_HasChildNodes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::CompositeNode::get_HasChildNodes method. Devuelve true si este nodo tiene nodos hijos en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


Devuelve **true** si este nodo tiene algún nodo hijo.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Ejemplos



Muestra cómo combinar las filas de dos tablas en una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// A continuación se presentan dos formas de obtener una tabla de un documento.
// 1 -  Desde la colección "Tables" de un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Usando el método "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Agregar todas las filas de la tabla actual a la siguiente.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Eliminar el contenedor de tabla vacío.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Ver también

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
