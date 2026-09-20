---
title: "Aspose::Words::Tables::CellFormat::ClearFormatting método"
linktitle: "ClearFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::CellFormat::ClearFormatting método. Restablece el formato de celda predeterminado. No cambia el ancho de la celda en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


Restablece el formato de celda predeterminado. No cambia el ancho de la celda.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
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

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
