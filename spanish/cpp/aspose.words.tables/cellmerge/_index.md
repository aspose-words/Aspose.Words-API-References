---
title: "enumeración Aspose::Words::Tables::CellMerge"
linktitle: "CellMerge"
second_title: "Referencia de API de Aspose.Words para C++"
description: "enumeración Aspose::Words::Tables::CellMerge. Especifica cómo se fusiona una celda en una tabla con otras celdas en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Especifica cómo se fusiona una celda en una tabla con otras celdas.

```cpp
enum class CellMerge
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | La celda no está fusionada. |
| First | 1 | La celda es la primera celda en un rango de celdas fusionadas. |
| Anterior | 2 | La celda se combina con la celda anterior horizontalmente o verticalmente. |


## Ejemplos



Muestra cómo combinar celdas de tabla verticalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una celda en la primera columna de la primera fila.
// Esta celda será la primera en un rango de celdas combinadas verticalmente.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Inserte una celda en la segunda columna de la primera fila, luego finalice la fila.
// Además, configure el generador para desactivar la combinación vertical en las celdas creadas.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Inserte una celda en la primera columna de la segunda fila.
// En lugar de agregar contenido de texto, combinaremos esta celda con la primera celda que añadimos directamente arriba.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Inserte otra celda independiente en la segunda columna de la segunda fila.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


Muestra cómo combinar celdas de tabla horizontalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una celda en la primera columna de la primera fila.
// Esta celda será la primera en un rango de celdas combinadas horizontalmente.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Inserte una celda en la segunda columna de la primera fila. En lugar de agregar contenido de texto,
// combinaremos esta celda con la primera celda que añadimos directamente a la izquierda.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Inserte dos celdas más sin combinar en la segunda fila.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Ver también

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
