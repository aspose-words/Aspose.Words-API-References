---
title: "Método Aspose::Words::DocumentBuilder::DeleteRow"
linktitle: "DeleteRow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::DeleteRow. Elimina una fila de una tabla en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Elimina una fila de una tabla.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableIndex | int32_t | El índice de la tabla. |
| rowIndex | int32_t | El índice de la fila en la tabla. |

### ReturnValue

El nodo de fila que acaba de eliminarse.
## Observaciones


Si el cursor está dentro de la fila que se está eliminando, el cursor se desplaza a la siguiente fila o al siguiente párrafo después de la tabla.

Si eliminas una fila de una tabla que contiene solo una fila, se elimina toda la tabla.

Para los parámetros de índice, cuando el índice es mayor o igual a 0, especifica un índice desde el principio, siendo 0 el primer elemento. Cuando el índice es menor que 0, especifica un índice desde el final, siendo -1 el último elemento.

## Ejemplos



Muestra cómo eliminar una fila de una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Elimina la primera fila de la primera tabla del documento.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Ver también

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
