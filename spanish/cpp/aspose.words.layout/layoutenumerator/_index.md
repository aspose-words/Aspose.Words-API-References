---
title: "Aspose::Words::Layout::LayoutEnumerator clase"
linktitle: "LayoutEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutEnumerator clase. Enumera entidades de diseño de página de un documento. Puede usar esta clase para recorrer el modelo de diseño de página. Las propiedades disponibles son tipo, geometría, texto e índice de página donde se renderiza la entidad, así como la estructura general y las relaciones. Use la combinación de GetEntity() y Current para mover a la entidad que corresponde a un nodo del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumera entidades de diseño de página de un documento. Puede usar esta clase para recorrer el modelo de diseño de página. Las propiedades disponibles son tipo, geometría, texto e índice de página donde se renderiza la entidad, así como la estructura general y las relaciones. Use la combinación de [GetEntity()](../) y [Current](./get_current/) para mover a la entidad que corresponde a un nodo del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Obtiene o establece la posición actual en el modelo de diseño de página. Esta propiedad devuelve un objeto opaco que corresponde a la entidad de diseño actual. |
| [get_Document](./get_document/)() const | Obtiene el documento que esta instancia enumera. |
| [get_Kind](./get_kind/)() | Obtiene el tipo de la entidad actual. Esto puede ser una cadena vacía pero nunca **null**. |
| [get_PageIndex](./get_pageindex/)() | Obtiene el índice basado en 1 de la página que contiene la entidad actual. |
| [get_Rectangle](./get_rectangle/)() | Devuelve el rectángulo delimitador de la entidad actual relativo a la esquina superior izquierda de la página (en puntos). |
| [get_Text](./get_text/)() | Obtiene el texto de la entidad span actual. Lanza una excepción para otros tipos de entidad. |
| [get_Type](./get_type/)() | Obtiene el tipo de la entidad actual. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene una propiedad con nombre de la entidad. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inicializa una nueva instancia de esta clase. |
| [MoveFirstChild](./movefirstchild/)() | Se mueve a la primera entidad hija. |
| [MoveLastChild](./movelastchild/)() | Se mueve a la última entidad hija. |
| [MoveNext](./movenext/)() | Se mueve a la siguiente entidad hermana en orden visual. Al iterar líneas de un párrafo dividido en varias páginas, este método no pasará a la página siguiente sino que se moverá a la siguiente entidad en la misma página. |
| [MoveNextLogical](./movenextlogical/)() | Se mueve a la siguiente entidad hermana en orden lógico. Al iterar líneas de un párrafo dividido en varias páginas, este método avanzará a la siguiente línea aunque se encuentre en otra página. |
| [MoveParent](./moveparent/)() | Se mueve a la entidad padre. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Se mueve a la entidad padre del tipo especificado. |
| [MovePrevious](./moveprevious/)() | Se mueve a la entidad hermana anterior. |
| [MovePreviousLogical](./movepreviouslogical/)() | Se mueve a la entidad hermana anterior en orden lógico. Al iterar líneas de un párrafo dividido en varias páginas, este método retrocederá a la línea anterior aunque se encuentre en otra página. |
| [Reset](./reset/)() | Mueve el enumerador a la primera página del documento. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Setter para [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
