---
title: "Clase Aspose::Words::Layout::LayoutCollector"
linktitle: "LayoutCollector"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Layout::LayoutCollector. Esta clase permite calcular los números de página de los nodos del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Esta clase permite calcular los números de página de los nodos del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Borra todos los datos de diseño recopilados. Llame a este método después de que el documento haya sido actualizado manualmente, o el diseño haya sido reconstruido. |
| [get_Document](./get_document/)() const | Obtiene o establece el documento al que está adjunta esta instancia del colector. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el índice basado en uno de la página donde termina el nodo. Devuelve 0 si el nodo no puede asignarse a una página. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve una posición opaca del [LayoutEnumerator](../layoutenumerator/) que corresponde al nodo especificado. Puede usar el valor devuelto como argumento para [Current](../layoutenumerator/get_current/) siempre que el documento que se está enumerando y el documento del nodo sean el mismo. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el número de páginas que abarca el nodo especificado. 0 si el nodo está dentro de una sola página. Esto es lo mismo que [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el índice basado en uno de la página donde comienza el nodo. Devuelve 0 si el nodo no puede asignarse a una página. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inicializa una instancia de esta clase. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Establecedor para [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Observaciones


Cuando crea un [LayoutCollector](./) y especifica un objeto [Document](../../aspose.words/document/) al que adjuntar, el colector registrará el mapeo de los nodos del documento a los objetos de diseño cuando el documento se formatee en páginas.

Podrá averiguar en qué página se encuentra un nodo de documento particular (p. ej., ejecución, párrafo o celda de tabla) usando los métodos [GetStartPageIndex()](../), [GetEndPageIndex()](../) y [GetNumPagesSpanned()](../). Estos métodos construyen automáticamente el modelo de diseño de página del documento y actualizan los campos si es necesario.

Cuando ya no necesite recopilar información de diseño, es mejor establecer la propiedad [Document](./get_document/) a **null** para evitar la recopilación innecesaria de más mapeos de diseño.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
