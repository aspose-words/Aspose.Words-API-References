---
title: "Método Aspose::Words::Tables::Table::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::EnsureMinimum. Si la tabla no tiene filas, crea y agrega una Row en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Si la tabla no tiene filas, crea y agrega una [Row](../../row/).

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Ejemplos



Muestra cómo asegurar que un nodo de tabla contenga los nodos que necesitamos para agregar contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Las tablas contienen filas, que contienen celdas, que pueden contener párrafos
// con elementos típicos como segmentos, formas y incluso otras tablas.
// Nuestra nueva tabla no tiene ninguno de estos nodos, y no podemos agregar contenido hasta que los tenga.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Llamar al método "EnsureMinimum" en una tabla garantizará que
// la tabla tiene al menos una fila y una celda con un párrafo vacío.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
