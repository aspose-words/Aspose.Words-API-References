---
title: "Aspose::Words::Tables::Row::get_IsLastRow método"
linktitle: "get_IsLastRow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Row::get_IsLastRow método. Verdadero si esta es la última fila en una tabla; falso en caso contrario en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


Verdadero si esta es la última fila en una tabla; falso en caso contrario.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
```


## Ejemplos



Muestra cómo configurar una tabla para que permanezca junta en la misma página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Habilitar KeepWithNext para cada párrafo en la tabla excepto para el
// los últimos en la última fila evitará que la tabla se divida en varias páginas.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## Ver también

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
