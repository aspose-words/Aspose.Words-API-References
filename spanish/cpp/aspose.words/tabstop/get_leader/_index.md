---
title: "Método get_Leader de Aspose::Words::TabStop"
linktitle: "get_Leader"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_Leader de Aspose::Words::TabStop. Obtiene o establece el tipo de línea líder mostrada bajo el carácter de tabulación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/tabstop/get_leader/
---
## TabStop::get_Leader method


Obtiene o establece el tipo de la línea guía mostrada bajo el carácter de tabulación.

```cpp
Aspose::Words::TabLeader Aspose::Words::TabStop::get_Leader() const
```


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

* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
