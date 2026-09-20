---
title: "Clase Aspose::Words::BookmarkStart"
linktitle: "BookmarkStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::BookmarkStart. Representa el inicio de un marcador en un documento Word. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/bookmarkstart/
---
## BookmarkStart class


Representa el inicio de un marcador en un documento Word. Para obtener más información, visite el artículo de documentación [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkStart : public Aspose::Words::Node,
                      public Aspose::Words::IBookmarkNode,
                      public Aspose::Words::IDisplaceableByCustomXml
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [BookmarkStart](./bookmarkstart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Inicializa una nueva instancia de la clase [BookmarkStart](./). |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_Bookmark](./get_bookmark/)() | Obtiene el objeto fachada que encapsula este inicio y fin de marcador. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_Name](./get_name/)() override | Obtiene el nombre del marcador. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [BookmarkStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Devuelve una cadena vacía. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | Establece el nombre del marcador. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Un marcador completo en un documento Word consta de un [BookmarkStart](./) y un [BookmarkEnd](../bookmarkend/) coincidente con el mismo nombre de marcador.

[BookmarkStart](./) and [BookmarkEnd](../bookmarkend/) are just markers inside a document that specify where the bookmark starts and ends.

Utilice la clase [Bookmark](./get_bookmark/) como una "fachada" para trabajar con un marcador como un único objeto.
## Ver también

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
