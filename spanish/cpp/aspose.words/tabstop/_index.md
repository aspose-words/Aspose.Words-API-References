---
title: "Clase Aspose::Words::TabStop"
linktitle: "TabStop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::TabStop. Representa una tabulación personalizada única. El objeto TabStop es un miembro de la colección TabStopCollection. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 68000
url: /es/cpp/aspose.words/tabstop/
---
## TabStop class


Representa una tabulación personalizada única. El objeto [TabStop](./) es un miembro de la colección [TabStopCollection](../tabstopcollection/). Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Compara con el [TabStop](./) especificado. |
| [get_Alignment](./get_alignment/)() const | Obtiene o establece la alineación del texto en este tabulador. |
| [get_IsClear](./get_isclear/)() | Devuelve **true** si este tabulador elimina cualquier tabulador existente en esta posición. |
| [get_Leader](./get_leader/)() const | Obtiene o establece el tipo de la línea guía mostrada bajo el carácter de tabulación. |
| [get_Position](./get_position/)() | Obtiene la posición del tabulador en puntos. |
| [GetHashCode](./gethashcode/)() const override | Calcula el código hash para este objeto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Método setter para [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Método setter para [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Inicializa una nueva instancia de esta clase. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Inicializa una nueva instancia de esta clase. |
| static [Type](./type/)() |  |
## Observaciones


Normalmente, un tabulador especifica una posición donde existe un tabulador. Pero como los tabuladores pueden heredarse de los estilos padre, puede ser necesario que el objeto hijo defina explícitamente que no hay tabulador en una posición dada. Para eliminar un tabulador heredado en una posición dada, cree un objeto [TabStop](./) y establezca [Alignment](./get_alignment/) a [Clear](../tabalignment/).

Para más información, vea [TabStopCollection](../tabstopcollection/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
