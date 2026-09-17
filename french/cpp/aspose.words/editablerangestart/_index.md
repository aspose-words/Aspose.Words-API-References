---
title: "Aspose::Words::EditableRangeStart class"
linktitle: "EditableRangeStart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::EditableRangeStart. Représente le début d'une plage modifiable dans un document Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words/editablerangestart/
---
## EditableRangeStart class


Représente le début d'une plage modifiable dans un document Word. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRangeStart : public Aspose::Words::Node,
                           public Aspose::Words::IDisplaceableByCustomXml,
                           public Aspose::Words::INodeWithAnnotationId
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_EditableRange](./get_editablerange/)() | Obtient l'objet façade qui encapsule le début et la fin de cette plage modifiable. |
| [get_Id](./get_id/)() const | Spécifie l'identifiant de la plage modifiable. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [EditableRangeStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Id](./set_id/)(int32_t) | Définisseur pour [Aspose::Words::EditableRangeStart::get_Id](./get_id/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Une plage modifiable complète dans un document Word se compose d'un [EditableRangeStart](./) et d'un [EditableRangeEnd](../editablerangeend/) correspondant avec le même Id.

[EditableRangeStart](./) and [EditableRangeEnd](../editablerangeend/) are just markers inside a document that specify where the editable range starts and ends.

Utilisez la classe [EditableRange](./get_editablerange/) comme une "facade" pour travailler avec une plage modifiable en tant qu'objet unique.


Actuellement, les plages modifiables ne sont prises en charge qu'au niveau en ligne, c'est‑à‑dire à l'intérieur du [Paragraph](../paragraph/), mais le début et la fin d'une plage modifiable peuvent se trouver dans des paragraphes différents.

## Voir aussi

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
