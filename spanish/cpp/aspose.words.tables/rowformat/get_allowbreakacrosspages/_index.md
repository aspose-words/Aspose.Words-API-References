---
title: "Método Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages. Verdadero si el texto en una fila de tabla puede dividirse a través de un salto de página en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Verdadero si se permite que el texto en una fila de tabla se divida en un salto de página.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Ejemplos



Muestra cómo desactivar la división de filas entre páginas para cada fila en una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Establezca la propiedad "AllowBreakAcrossPages" en "false" para mantener la fila
// en una sola pieza si una tabla abarca dos páginas, lo que se rompería a lo largo de esa fila.
// Si la fila es demasiado grande para caber en una página, Microsoft Word la moverá a la siguiente página.
// Establezca la propiedad "AllowBreakAcrossPages" en "true" para permitir que la fila se divida entre dos páginas.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Ver también

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
