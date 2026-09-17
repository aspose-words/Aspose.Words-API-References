---
title: "Méthode Aspose::Words::DocumentBuilder::get_CurrentNode"
linktitle: "get_CurrentNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::get_CurrentNode. Obtient le nœud actuellement sélectionné dans ce DocumentBuilder en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/documentbuilder/get_currentnode/
---
## DocumentBuilder::get_CurrentNode method


Obtient le nœud actuellement sélectionné dans ce [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::get_CurrentNode()
```

## Remarques


[CurrentNode](./) is a cursor of [DocumentBuilder](../) and points to a [Node](../../node/) that is a direct child of a [Paragraph](../../paragraph/). Any insert operations you perform using [DocumentBuilder](../) will insert before the [CurrentNode](./).

Lorsque le paragraphe actuel est vide ou que le curseur est positionné juste avant la fin d’un paragraphe ou d’une balise de document structuré, [CurrentNode](./) renvoie **null**.

## Exemples



Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un signet valide, une entité qui consiste en des nœuds entourés par un nœud de début de signet,
// et un nœud de fin de signet.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Le curseur du DocumentBuilder est toujours en avance sur le nœud que nous avons ajouté en dernier avec lui.
// Si le curseur du builder se trouve à la fin du document, son nœud actuel sera null.
// Le nœud précédent est le nœud de fin de signet que nous avons ajouté en dernier.
// L'ajout de nouveaux nœuds avec le builder les ajoutera au dernier nœud.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Si nous souhaitons modifier une autre partie du document avec le builder,
// nous devrons amener son curseur au nœud que nous souhaitons modifier.
builder->MoveToBookmark(u"MyBookmark");

// Le déplacer vers un signet le déplacera vers le premier nœud situé entre les nœuds de début et de fin du signet, le segment encapsulé.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Nous pouvons également déplacer le curseur vers un nœud individuel ainsi.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Nous pouvons utiliser des méthodes spécifiques pour nous déplacer vers le début/la fin d'un document.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## Voir aussi

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
