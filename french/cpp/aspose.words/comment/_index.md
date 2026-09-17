---
title: "Aspose::Words::Comment class"
linktitle: "Comment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment class. Représente un conteneur pour le texte d'un commentaire. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/comment/
---
## Comment class


Représente un conteneur pour le texte d'un commentaire. Pour en savoir plus, consultez l'article de documentation [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du commentaire. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du commentaire. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Ajoute une réponse à ce commentaire. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialise une nouvelle instance de la classe [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Initialise une nouvelle instance de la classe [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Si le dernier enfant n’est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [get_Ancestor](./get_ancestor/)() | Renvoie l'objet [Comment](./) parent. Renvoie **null** pour les commentaires de niveau supérieur. |
| [get_Author](./get_author/)() const | Renvoie ou définit le nom de l'auteur d'un commentaire. |
| [get_Count](../compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_DateTime](./get_datetime/)() const | Obtient la date et l'heure auxquelles le commentaire a été fait. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Obtient la date et l'heure UTC auxquelles le commentaire a été fait. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Done](./get_done/)() const | Obtient ou définit le drapeau indiquant que le commentaire a été marqué comme terminé. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Obtient le premier paragraphe de l'histoire. |
| [get_Font](../inlinestory/get_font/)() | Fournit l’accès au formatage de police du caractère d’ancrage de cet objet. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_Id](./get_id/)() const | Obtient ou définit l'identifiant du commentaire. |
| [get_Initial](./get_initial/)() const | Renvoie ou définit les initiales de l'utilisateur associé à un commentaire spécifique. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Obtient le dernier paragraphe de l'histoire. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [get_ParentId](./get_parentid/)() const | Obtient l'ID du commentaire parent. Une valeur de **%-1** signifie que le commentaire n'a pas de parent. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Récupère le [Paragraph](../paragraph/) parent de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_Replies](./get_replies/)() | Renvoie une collection d'objets [Comment](./) qui sont les enfants immédiats du commentaire spécifié. |
| [get_StoryType](./get_storytype/)() override | Renvoie [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](../compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveAllReplies](./removeallreplies/)() | Supprime toutes les réponses à ce commentaire. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Supprime la réponse spécifiée à ce commentaire. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_Author](./set_author/)(const System::String\&) | Mutateur pour [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Obtient la date et l'heure auxquelles le commentaire a été fait. |
| [set_Done](./set_done/)(bool) | Mutateur pour [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Mutateur pour [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Mutateur pour [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Définit l'ID du commentaire parent. Une valeur de **%-1** signifie que le commentaire n'a pas de parent. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Un commentaire est une annotation ancrée à une région de texte ou à une position dans le texte. Un commentaire peut contenir une quantité arbitraire de contenu au niveau du bloc.

Si un objet [Comment](./) apparaît seul, le commentaire est ancré à la position de l'objet [Comment](./).

Pour ancrer un commentaire à une région de texte, trois objets sont nécessaires : [Comment](./), [CommentRangeStart](../commentrangestart/) et [CommentRangeEnd](../commentrangeend/). Les trois objets doivent partager la même valeur de [Id](./get_id/).

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Exemples



Montre comment ajouter un commentaire à un document, puis y répondre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Placez le commentaire à un nœud dans le corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge droite de la page, et avec une ligne pointillée le reliant à son paragraphe.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Ajoutez une réponse, qui apparaîtra sous le commentaire parent.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Les commentaires et les réponses sont tous deux des nœuds Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Les commentaires qui ne répondent pas à d'autres commentaires sont "top-level". Ils n'ont aucun commentaire ancêtre.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Les réponses ont un commentaire ancêtre de niveau supérieur.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Montre comment ajouter un commentaire à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// Dans Microsoft Word, nous pouvons cliquer avec le bouton droit sur ce commentaire dans le corps du document pour le modifier, ou y répondre.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Voir aussi

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
