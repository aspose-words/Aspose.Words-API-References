---
title: "Aspose::Words::Tables::Row::EnsureMinimum método"
linktitle: "EnsureMinimum"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Row::EnsureMinimum método. Si la Row no tiene celdas, crea y agrega una Cell en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Si la [Row](../) no tiene celdas, crea y agrega una [Cell](../../cell/).

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Ejemplos



Muestra cómo asegurar que un nodo fila contenga los nodos que necesitamos para comenzar a agregar contenido a él.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Las filas contienen celdas, que contienen párrafos con elementos típicos como runs, shapes y hasta otras tablas.
// Nuestra nueva fila no tiene ninguno de estos nodos, y no podemos agregar contenido a ella hasta que los tenga.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Llamar al método "EnsureMinimum" en una tabla garantizará que
// La tabla tiene al menos una celda con un párrafo vacío.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ver también

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
