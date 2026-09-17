---
title: "Aspose::Words::BookmarkStart classe"
linktitle: "BookmarkStart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BookmarkStart classe. Représente le début d'un signet dans un document Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/bookmarkstart/
---
## BookmarkStart class


Représente le début d'un signet dans un document Word. Pour en savoir plus, consultez l'article de documentation [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkStart : public Aspose::Words::Node,
                      public Aspose::Words::IBookmarkNode,
                      public Aspose::Words::IDisplaceableByCustomXml
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [BookmarkStart](./bookmarkstart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Initialise une nouvelle instance de la classe [BookmarkStart](./). |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_Bookmark](./get_bookmark/)() | Obtient l'objet façade qui encapsule ce début et cette fin de signet. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_Name](./get_name/)() override | Obtient le nom du signet. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [BookmarkStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Renvoie une chaîne vide. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | Définit le nom du signet. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Un signet complet dans un document Word se compose d'un [BookmarkStart](./) et d'un [BookmarkEnd](../bookmarkend/) correspondant avec le même nom de signet.

[BookmarkStart](./) and [BookmarkEnd](../bookmarkend/) are just markers inside a document that specify where the bookmark starts and ends.

Utilisez la classe [Bookmark](./get_bookmark/) comme une "façade" pour travailler avec un signet en tant qu'objet unique.
## Voir aussi

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
