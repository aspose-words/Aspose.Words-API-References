---
title: "Método Aspose::Words::NodeCollection::Clear"
linktitle: "Clear"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeCollection::Clear. Elimina todos los nodos de esta colección y del documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Elimina todos los nodos de esta colección y del documento.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Ejemplos



Muestra cómo eliminar todas las secciones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Este documento tiene una sección con algunos nodos hijos que contienen y muestran todo el contenido del documento.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Limpia la colección de secciones, lo que eliminará todos los hijos del documento.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Ver también

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
