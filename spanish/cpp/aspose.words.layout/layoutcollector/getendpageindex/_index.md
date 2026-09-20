---
title: "Aspose::Words::Layout::LayoutCollector::GetEndPageIndex método"
linktitle: "GetEndPageIndex"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutCollector::GetEndPageIndex método. Obtiene el índice basado en 1 de la página donde termina el nodo. Devuelve 0 si el nodo no puede asignarse a una página en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector::GetEndPageIndex method


Obtiene el índice basado en uno de la página donde termina el nodo. Devuelve 0 si el nodo no puede asignarse a una página.

```cpp
int32_t Aspose::Words::Layout::LayoutCollector::GetEndPageIndex(const System::SharedPtr<Aspose::Words::Node> &node)
```


## Ejemplos



Muestra cómo ver los rangos de páginas que abarca un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Llame al método "GetNumPagesSpanned" para contar cuántas páginas abarca el contenido de nuestro documento.
// Dado que el documento está vacío, ese número de páginas es actualmente cero.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Rellene el documento con 5 páginas de contenido.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Antes del colector de diseño, necesitamos llamar al método "UpdatePageLayout" para darnos
// una cifra precisa para cualquier métrica relacionada con el diseño, como el recuento de páginas.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Podemos ver los números de las páginas de inicio y fin de cualquier nodo y sus rangos de página totales.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Podemos iterar sobre las entidades de diseño usando un LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// El LayoutEnumerator puede recorrer la colección de entidades de diseño como un árbol.
// También podemos aplicarlo a la entidad de diseño correspondiente de cualquier nodo.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Ver también

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
