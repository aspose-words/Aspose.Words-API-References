---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method"
linktitle: "GetChildNodes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method. Devuelve una colección en tiempo real de nodos secundarios que coinciden con los tipos especificados en C++."
type: docs
weight: 14500
url: /es/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Devuelve una colección en vivo de nodos hijos que coinciden con los tipos especificados.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
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

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
