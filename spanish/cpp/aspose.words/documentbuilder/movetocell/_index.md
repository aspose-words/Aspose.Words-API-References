---
title: "Método Aspose::Words::DocumentBuilder::MoveToCell"
linktitle: "MoveToCell"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::MoveToCell. Mueve el cursor a una celda de tabla en la sección actual en C++."
type: docs
weight: 53000
url: /es/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Mueve el cursor a una celda de tabla en la sección actual.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableIndex | int32_t | El índice de la tabla a la que moverse. |
| rowIndex | int32_t | El índice de la fila en la tabla. |
| columnIndex | int32_t | El índice de la columna en la tabla. |
| characterIndex | int32_t | El índice del carácter dentro de la celda. Un valor negativo permite especificar una posición desde el final de la celda. Use -1 para moverse al final de la celda. |
## Observaciones


La navegación se realiza dentro de la historia actual de la sección actual.

Para los parámetros de índice, cuando el índice es mayor o igual a 0, especifica un índice desde el principio, siendo 0 el primer elemento. Cuando el índice es menor que 0, especifica un índice desde el final, siendo -1 el último elemento.

## Ejemplos



Muestra cómo mover el cursor de DocumentBuilder a una celda en una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree una tabla vacía de 2x2.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Porque hemos finalizado la tabla con el método EndTable,
// el cursor de DocumentBuilder está actualmente fuera de la tabla.
// Este cursor tiene la misma función que el cursor intermitente de texto de Microsoft Word.
// También puede moverse a una ubicación diferente en el documento usando los métodos MoveTo del builder.
// Podemos mover el cursor de nuevo dentro de la tabla a una celda específica.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
