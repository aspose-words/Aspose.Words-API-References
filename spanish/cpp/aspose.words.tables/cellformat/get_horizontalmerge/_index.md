---
title: "Método Aspose::Words::Tables::CellFormat::get_HorizontalMerge"
linktitle: "get_HorizontalMerge"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::CellFormat::get_HorizontalMerge. Especifica cómo se combina la celda horizontalmente con otras celdas en la fila en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Especifica cómo se fusiona la celda horizontalmente con otras celdas en la fila.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Ejemplos



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
