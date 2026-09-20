---
title: "Aspose::Words::Markup::SmartTag class"
linktitle: "SmartTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SmartTag class. Este elemento especifica la presencia de una etiqueta inteligente alrededor de una o más estructuras en línea (corridas, imágenes, campos, etc.) dentro de un párrafo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.markup/smarttag/
---
## SmartTag class


Este elemento especifica la presencia de una etiqueta inteligente alrededor de una o más estructuras en línea (runs, images, fields, etc.) dentro de un párrafo. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SmartTag : public Aspose::Words::CompositeNode,
                 public Aspose::Words::Markup::IMarkupNode
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del [SmartTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del [SmartTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Element](./get_element/)() const | Especifica el nombre de la etiqueta inteligente dentro del documento. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [SmartTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Properties](./get_properties/)() const | Una colección de las propiedades de la etiqueta inteligente. |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Uri](./get_uri/)() const | Especifica el URI del espacio de nombres de la etiqueta inteligente. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos hijos del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](./) del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../../aspose.words/node/) que coincide con la expresión XPath. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Element](./set_element/)(const System::String\&) | Método set para [Aspose::Words::Markup::SmartTag::get_Element](./get_element/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Uri](./set_uri/)(const System::String\&) | Método set para [Aspose::Words::Markup::SmartTag::get_Uri](./get_uri/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inicializa una nueva instancia de la clase [SmartTag](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Las etiquetas inteligentes son un tipo de marcado XML personalizado. Las etiquetas inteligentes ofrecen una funcionalidad para incrustar semántica definida por el cliente en el documento mediante la capacidad de proporcionar un espacio de nombres/nombre básico para una ejecución o conjunto de ejecuciones dentro de un documento.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

La lista completa de nodos hijos que pueden aparecer dentro de una etiqueta inteligente está compuesta por [BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [CommentRangeStart](../../aspose.words/commentrangestart/), [CommentRangeEnd](../../aspose.words/commentrangeend/), [SmartTag](./).
## Ver también

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
