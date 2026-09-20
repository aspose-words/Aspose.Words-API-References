---
title: "Aspose::Words::SpecialChar clase"
linktitle: "SpecialChar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SpecialChar clase. Clase base para caracteres especiales en el documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 62000
url: /es/cpp/aspose.words/specialchar/
---
## SpecialChar class


Clase base para caracteres especiales en el documento. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class SpecialChar : public Aspose::Words::Inline
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Font](../inline/get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [SpecialChar](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Recupera el [Paragraph](../paragraph/) padre de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Obtiene el carácter especial que representa este nodo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Un documento de Microsoft Word puede incluir varios caracteres especiales que representan campos, campos de formulario, formas, objetos OLE, notas al pie, etc. Para la lista de caracteres especiales vea [ControlChar](../controlchar/).

[SpecialChar](./) is an inline-node and can only be a child of [Paragraph](../paragraph/).

[SpecialChar](./) char is used as a base class for more specific classes that represent special characters that Aspose.Words provides programmatic access for. The [SpecialChar](./) class is also used itself to represent special character for which Aspose.Words does not provide detailed programmatic access. 
## Ver también

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
