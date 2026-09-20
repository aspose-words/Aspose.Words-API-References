---
title: "Aspose::Words::Paragraph::get_IsInCell método"
linktitle: "get_IsInCell"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Paragraph::get_IsInCell método. Verdadero si este párrafo es un hijo inmediato de Cell; falso en caso contrario en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


Verdadero si este párrafo es un hijo inmediato de [Cell](../../../aspose.words.tables/cell/); falso en caso contrario.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
