---
title: "Clase Aspose::Words::Lists::ListLabel"
linktitle: "ListLabel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Lists::ListLabel. Define propiedades específicas de una etiqueta de lista. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.lists/listlabel/
---
## ListLabel class


Define propiedades específicas de una etiqueta de lista. Para obtener más información, visite el artículo de documentación [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLabel : public Aspose::Words::IRunAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Obtiene la fuente de la etiqueta de lista. |
| [get_LabelString](./get_labelstring/)() | Obtiene una representación en cadena de la etiqueta de lista. |
| [get_LabelValue](./get_labelvalue/)() | Obtiene un valor numérico para esta etiqueta. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo extraer las etiquetas de lista de todos los párrafos que son elementos de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Encuentre si tenemos la lista del párrafo. En nuestro documento, nuestra lista usa números arábigos simples,
// que comienzan en tres y terminan en seis.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Este es el texto que obtenemos al exportar este nodo al formato de texto.
    // Esta salida de texto omitirá las etiquetas de lista. Recorte cualquier carácter de formato de párrafo.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Esto obtiene la posición del párrafo en el nivel actual de la lista. Si tenemos una lista con varios niveles,
    // esto nos indicará en qué posición está en ese nivel.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Combínelos para incluir la etiqueta de lista con el texto en la salida.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## Ver también

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
