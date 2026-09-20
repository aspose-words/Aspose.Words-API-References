---
title: "Aspose::Words::Tables::Cell::EnsureMinimum método"
linktitle: "EnsureMinimum"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Cell::EnsureMinimum método. Si el último hijo no es un párrafo, crea y agrega un párrafo vacío en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Si el último hijo no es un párrafo, crea y agrega un párrafo vacío.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Ejemplos



Muestra cómo asegurar que un nodo celda contenga los nodos que necesitamos para comenzar a agregar contenido a él.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Las celdas pueden contener párrafos con elementos típicos como ejecuciones, formas y hasta otras tablas.
// Nuestra nueva celda no tiene párrafos, y no podemos agregar contenidos como nodos de ejecución y forma hasta que los tenga.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Llamar al método "EnsureMinimum" en una celda garantizará que
// la celda tenga al menos un párrafo vacío, al que luego podemos agregar contenidos.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ver también

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
