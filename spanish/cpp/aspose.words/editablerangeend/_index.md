---
title: "Clase Aspose::Words::EditableRangeEnd"
linktitle: "EditableRangeEnd"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::EditableRangeEnd. Representa el final de un rango editable en un documento Word. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words/editablerangeend/
---
## EditableRangeEnd class


Representa el final de un rango editable en un documento Word. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRangeEnd : public Aspose::Words::Node,
                         public Aspose::Words::IDisplaceableByCustomXml,
                         public Aspose::Words::INodeWithAnnotationId
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_EditableRangeStart](./get_editablerangestart/)() | Correspondiente [EditableRangeStart](../editablerangestart/), recibido por ID. |
| [get_Id](./get_id/)() const | Especifica el identificador del rango editable. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [EditableRangeEnd](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Id](./set_id/)(int32_t) | Establecedor de [Aspose::Words::EditableRangeEnd::get_Id](./get_id/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Un rango editable completo en un documento Word consta de un [EditableRangeStart](./get_editablerangestart/) y un [EditableRangeEnd](./) coincidente con el mismo Id.

[EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./) are just markers inside a document that specify where the editable range starts and ends.

Utilice la clase [EditableRange](../editablerange/) como una "fachada" para trabajar con un rango editable como un único objeto.


Actualmente los rangos editables solo se admiten a nivel inline, es decir, dentro de [Paragraph](../paragraph/), pero el inicio y el final del rango editable pueden estar en diferentes párrafos.

## Ver también

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
