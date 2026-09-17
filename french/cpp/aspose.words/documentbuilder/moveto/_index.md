---
title: "Méthode Aspose::Words::DocumentBuilder::MoveTo"
linktitle: "MoveTo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::MoveTo. Déplace le curseur vers un nœud en ligne ou vers la fin d'un paragraphe en C++."
type: docs
weight: 51000
url: /fr/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Déplace le curseur vers un nœud en ligne ou vers la fin d'un paragraphe.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nœud | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud doit être un paragraphe ou un enfant direct d'un paragraphe. |
## Remarques


Lorsque *node* est un nœud de niveau en ligne, le curseur est déplacé vers ce nœud et le contenu supplémentaire sera inséré avant ce nœud.

Lorsque *node* est un [Paragraph](../../paragraph/), le curseur est déplacé à la fin du paragraphe et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

Lorsque *node* est un nœud de niveau bloc mais pas un [Paragraph](../../paragraph/), le curseur est déplacé à la fin du premier paragraphe du nœud de niveau bloc et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

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


Montre comment déplacer la position du curseur d'un [DocumentBuilder](../) vers un nœud spécifié.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Le constructeur de document possède un curseur, qui agit comme la partie du document
// où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de document.
// Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
// et il se place également **toujours** **après** tout **nœud** que le constructeur vient d'insérer.
// Pour ajouter du contenu à une autre partie du document,
// nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
// L'ajout d'un deuxième run l'insérera devant le premier run.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Voir aussi

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
