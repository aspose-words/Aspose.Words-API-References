---
title: "Aspose::Words::AbsolutePositionTab classe"
linktitle: "AbsolutePositionTab"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AbsolutePositionTab classe. Un onglet de position absolue est un caractère utilisé pour avancer la position sur la ligne actuelle de texte lors de l’affichage de ce contenu WordprocessingML. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class


Une tabulation à position absolue est un caractère utilisé pour avancer la position sur la ligne de texte actuelle lors de l'affichage de ce contenu WordprocessingML. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class AbsolutePositionTab : public Aspose::Words::SpecialChar
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Font](../inline/get_font/)() | Fournit l'accès au format de police de cet objet. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](../specialchar/get_nodetype/)() const override | Renvoie [SpecialChar](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Récupère le [Paragraph](../paragraph/) parent de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](../specialchar/gettext/)() override | Obtient le caractère spécial que ce nœud représente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [SpecialChar](../specialchar/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
