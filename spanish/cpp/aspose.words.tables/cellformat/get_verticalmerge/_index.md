---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge método"
linktitle: "get_VerticalMerge"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge método. Especifica cómo la celda se combina con otras celdas verticalmente en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Especifica cómo se fusiona la celda con otras celdas verticalmente.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Observaciones


Las celdas solo pueden combinarse verticalmente si sus límites izquierdo y derecho son idénticos.

Cuando las celdas se combinan verticalmente, las áreas de visualización de las celdas combinadas se consolidan. El área consolidada se usa para mostrar el contenido de la primera celda combinada verticalmente y todas las demás celdas combinadas verticalmente deben estar vacías.

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

## Ver también

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
