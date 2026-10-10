---
title: "Aspose::Words::Range::Delete método"
linktitle: "Eliminar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Range::Delete método. Elimina todos los caracteres del rango en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/range/delete/
---
## Range::Delete method


Elimina todos los caracteres del rango.

```cpp
void Aspose::Words::Range::Delete()
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

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
