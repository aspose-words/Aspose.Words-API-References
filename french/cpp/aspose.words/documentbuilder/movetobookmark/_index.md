---
title: "Méthode Aspose::Words::DocumentBuilder::MoveToBookmark"
linktitle: "MoveToBookmark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::MoveToBookmark. Déplace le curseur vers un signet en C++."
type: docs
weight: 52000
url: /fr/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Déplace le curseur vers un signet.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Le nom du signet vers lequel déplacer le curseur. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Remarques


Déplace le curseur à une position juste après le début du signet portant le nom spécifié.

La comparaison n’est pas sensible à la casse. Si le signet n’est pas trouvé, **false** est retourné et le curseur n’est pas déplacé.

L'insertion d'un nouveau texte ne remplace pas le texte existant du signet.

Notez que certains signets dans le document sont affectés à des champs de formulaire. Se déplacer vers un tel signet et y insérer du texte insère le texte dans le code du champ de formulaire. Bien que cela n'invalide pas le champ de formulaire, le texte inséré ne sera pas visible car il devient partie du code du champ.

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
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Déplace le curseur vers un signet avec une plus grande précision.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Le nom du signet vers lequel déplacer le curseur. |
| isStart | bool | Lorsque **true**, déplace le curseur au début du signet. Lorsque **false**, déplace le curseur à la fin du signet. |
| isAfter | bool | Lorsque **true**, déplace le curseur pour qu'il soit après la position de début ou de fin du signet. Lorsque **false**, déplace le curseur pour qu'il soit avant la position de début ou de fin du signet. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Remarques


Déplace le curseur à une position avant ou après le début ou la fin du signet.

Si la position souhaitée n'est pas au niveau en ligne, déplace au paragraphe suivant.

La comparaison n’est pas sensible à la casse. Si le signet n’est pas trouvé, **false** est retourné et le curseur n’est pas déplacé.

## Exemples



Montre comment déplacer le curseur du point d'insertion de nœud d'un DocumentBuilder vers un signet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un signet valide se compose d'un nœud BookmarkStart, d'un nœud BookmarkEnd avec un
// nom de signet correspondant quelque part après, et le contenu entouré par ces nœuds.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Il existe 4 façons de déplacer le curseur d'un DocumentBuilder vers un signet.
// Si nous sommes entre les nœuds BookmarkStart et BookmarkEnd, le curseur sera à l'intérieur du signet.
// Cela signifie que tout texte ajouté par le builder deviendra une partie du signet.
// 1 -  À l'extérieur du signet, devant le nœud BookmarkStart :
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  À l'intérieur du signet, juste après le nœud BookmarkStart :
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  À l'intérieur du signet, juste devant le nœud BookmarkEnd :
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  À l'extérieur du signet, après le nœud BookmarkEnd :
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
