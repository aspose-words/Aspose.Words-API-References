---
title: "Método Aspose::Words::TabStopCollection::RemoveByPosition"
linktitle: "RemoveByPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::TabStopCollection::RemoveByPosition. Elimina una tabulación en la posición especificada de la colección en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


Elimina una tabulación en la posición especificada de la colección.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double | La posición (en puntos) de la tabulación a eliminar. |

## Ejemplos



Muestra cómo modificar la posición del tabulador derecho en párrafos relacionados con la TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Itere a través de todos los párrafos con estilos basados en resultados de la TOC; este es cualquier estilo entre TOC y TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Obtenga el primer tabulador usado en este párrafo, que debería ser el tabulador usado para alinear los números de página.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Reemplace el primer tabulador predeterminado con un tabulador personalizado.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Ver también

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
