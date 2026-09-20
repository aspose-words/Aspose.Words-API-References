---
title: "Método Aspose::Words::NodeCollection::RemoveAt"
linktitle: "RemoveAt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeCollection::RemoveAt. Elimina el nodo en el índice especificado de la colección y del documento en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Elimina el nodo en el índice especificado de la colección y del documento.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero del nodo. Se permiten índices negativos y indican acceso desde el final de la lista. Por ejemplo, -1 significa el último nodo, -2 el penúltimo y así sucesivamente. |

## Ejemplos



Muestra cómo agregar y eliminar secciones en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimine la primera sección del documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Añada una copia de lo que ahora es la primera sección al final del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Ver también

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
