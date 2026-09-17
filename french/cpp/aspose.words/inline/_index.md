---
title: "Aspose::Words::Inline classe"
linktitle: "Inline"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Inline classe. Classe de base pour les nœuds de niveau en ligne qui peuvent avoir un format de caractères associé, mais ne peuvent pas avoir de nœuds enfants. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/inline/
---
## Inline class


Classe de base pour les nœuds de niveau en ligne pouvant avoir un formatage de caractères associé, mais ne pouvant pas avoir de nœuds enfants. Pour en savoir plus, consultez l'article de documentation [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepte un visiteur. |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Font](./get_font/)() | Fournit l'accès au format de police de cet objet. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Obtient le type de ce nœud. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](./get_parentparagraph/)() | Récupère le [Paragraph](../paragraph/) parent de ce nœud. |
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
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Une classe dérivée de [Inline](./) peut être un enfant de [Paragraph](../paragraph/).

## Exemples



Montre comment déterminer le type de révision d'un nœud en ligne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
// est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
// Lors de l'édition d'un document avec Aspose.Words, nous pouvons commencer le suivi des révisions en
// appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
// Nous pouvons soit accepter les révisions pour les intégrer au document
// ou les rejeter afin de modifier efficacement le changement proposé.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Le nœud parent d'une révision est le run auquel la révision se rapporte. Un Run est un nœud Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Ci-dessous se trouvent cinq types de révisions qui peuvent marquer un nœud Inline.
// 1 -  Une révision "insert" :
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Une révision "format" :
// Cette révision se produit lorsque nous modifions le formatage du texte tout en suivant les modifications.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Une révision "move from" :
// Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
// tout en suivant les modifications, deux révisions apparaissent.
// La révision "move from" est une copie du texte original avant que nous le déplacions.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Une révision "move to" :
// La révision "move to" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
// et conserve le texte de la révision "move to".
// Rejeter une révision de déplacement, au contraire, conserve la révision "move from" et supprime la révision "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Une révision "delete" :
// Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
// il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions,
// ce qui supprimera définitivement le texte, ou que nous rejetions la révision, ce qui conservera le texte que nous avons supprimé à son emplacement d'origine.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Voir aussi

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
