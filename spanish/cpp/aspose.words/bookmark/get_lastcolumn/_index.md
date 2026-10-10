---
title: "Aspose::Words::Bookmark::get_LastColumn método"
linktitle: "get_LastColumn"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Bookmark::get_LastColumn método. Obtiene el índice basado en cero de la última columna del rango de columnas de tabla asociado al marcador en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/bookmark/get_lastcolumn/
---
## Bookmark::get_LastColumn method


Obtiene el índice basado en cero de la última columna del rango de columnas de tabla asociado al marcador.

```cpp
int32_t Aspose::Words::Bookmark::get_LastColumn()
```


## Ejemplos



Muestra cómo obtener información sobre los marcadores de columnas de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Si un marcador engloba columnas de una tabla, es un marcador de columna de tabla, y su bandera IsColumn se establece en true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Imprima el contenido de la primera y última columnas englobadas por el marcador.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Ver también

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
