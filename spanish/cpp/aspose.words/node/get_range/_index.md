---
title: "Método Aspose::Words::Node::get_Range"
linktitle: "get_Range"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_Range. Devuelve un objeto Range que representa la parte de un documento que está contenida en este nodo en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Devuelve un objeto [Range](../../range/) que representa la parte de un documento que está contenida en este nodo.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## Ejemplos



Muestra cómo eliminar todos los nodos de un rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega texto a la primera sección del documento y luego agrega otra sección.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Elimina la primera sección por completo al eliminar todos los nodos
// dentro de su rango, incluida la propia sección.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Ver también

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
