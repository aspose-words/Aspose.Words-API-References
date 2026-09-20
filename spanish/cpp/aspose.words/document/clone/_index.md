---
title: "Aspose::Words::Document::Clone método"
linktitle: "Clonar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::Clone método. Realiza una copia profunda del Document en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/document/clone/
---
## Document::Clone method


Realiza una copia profunda del [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

El documento clonado.

## Ejemplos



Muestra cómo clonar profundamente un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Clonar producirá un nuevo documento con el mismo contenido que el original,
// pero con una copia única de cada uno de los nodos del documento original.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Ver también

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
