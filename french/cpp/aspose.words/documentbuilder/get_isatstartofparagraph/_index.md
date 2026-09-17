---
title: "Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph méthode"
linktitle: "get_IsAtStartOfParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph méthode. Retourne true si le curseur est au début du paragraphe actuel (aucun texte avant le curseur) en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/documentbuilder/get_isatstartofparagraph/
---
## DocumentBuilder::get_IsAtStartOfParagraph method


Renvoie **true** si le curseur est au début du paragraphe actuel (aucun texte avant le curseur).

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph()
```


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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
