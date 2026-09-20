---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly método"
linktitle: "RemoveSelfOnly"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly método. Elimina solo este nodo SDT, pero mantiene su contenido dentro del árbol del documento en C++."
type: docs
weight: 17500
url: /es/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
```


## Ejemplos



Muestra cómo eliminar la etiqueta de documento estructurado, pero mantiene el contenido interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Esta colección proporciona una interfaz unificada para acceder a etiquetas estructuradas con rango y sin rango.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Aquí podemos obtener nodos hijos desde la interfaz común de etiquetas estructuradas con rango y sin rango.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Ver también

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
