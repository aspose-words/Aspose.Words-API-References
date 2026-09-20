---
title: "Aspose::Words::Notes::FootnoteSeparator class"
linktitle: "FootnoteSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteSeparator class. Representa un contenedor para el separador de nota al pie/nota al final y el contenido de continuación de un documento en C++."
type: docs
weight: 3334
url: /es/cpp/aspose.words.notes/footnoteseparator/
---
## FootnoteSeparator class


Representa un contenedor para el separador de notas al pie/al final y el contenido de continuación de un documento.

```cpp
class FootnoteSeparator : public Aspose::Words::Story
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Cuando se implementa en una clase derivada, llama al método VisitXXXEnd del visitante de documento especificado. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Cuando se implementa en una clase derivada, llama al método VisitXXXStart del visitante de documento especificado. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(const System::String\&) | Un método abreviado que crea un objeto [Paragraph](../../aspose.words/paragraph/) con texto opcional y lo agrega al final de este objeto. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Elimina todas las formas del texto de esta historia. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FirstParagraph](../../aspose.words/story/get_firstparagraph/)() override | Obtiene el primer párrafo de la historia. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_LastParagraph](../../aspose.words/story/get_lastparagraph/)() override | Obtiene el último párrafo de la historia. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Obtiene el tipo de este nodo. |
| [get_Paragraphs](../../aspose.words/story/get_paragraphs/)() override | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_SeparatorType](./get_separatortype/)() const |  |
| [get_StoryType](../../aspose.words/story/get_storytype/)() override | Obtiene el tipo de esta historia. |
| [get_Tables](../../aspose.words/story/get_tables/)() override | Obtiene una colección de tablas que son hijos inmediatos de la historia. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](../../aspose.words.markup/smarttag/) del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../../aspose.words/node/) que coincide con la expresión XPath. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


[FootnoteSeparator](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

Solo puede haber un [FootnoteSeparator](./) de cada [FootnoteSeparatorType](../footnoteseparatortype/) en un documento.

## Ejemplos



Muestra cómo administrar el formato del separador de notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Alinear el separador de notas al pie.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ver también

* Class [Story](../../aspose.words/story/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
