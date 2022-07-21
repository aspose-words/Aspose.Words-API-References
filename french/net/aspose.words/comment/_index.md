---
title: Comment
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente un conteneur pour le texte dun commentaire.
type: docs
weight: 220
url: /fr/net/aspose.words/comment/
---
## Comment class

Représente un conteneur pour le texte d'un commentaire.

```csharp
public sealed class Comment : InlineStory
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Comment](comment#constructor)(DocumentBase) | Initialise une nouvelle instance du **Commentaire** classe. |
| [Comment](comment#constructor_1)(DocumentBase, string, string, DateTime) | Initialise une nouvelle instance du **Commentaire** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor) { get; } | Renvoie l'objet Commentaire parent. Renvoie null pour les commentaires de niveau supérieur. |
| [Author](../../aspose.words/comment/author) { get; set; } | Renvoie ou définit le nom de l'auteur d'un commentaire. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DateTime](../../aspose.words/comment/datetime) { get; set; } | Obtient la date et l'heure auxquelles le commentaire a été fait. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtient le document auquel ce nœud appartient. |
| [Done](../../aspose.words/comment/done) { get; set; } | Obtient ou définit un indicateur indiquant que le commentaire a été marqué comme terminé. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Obtient le premier paragraphe de l'histoire. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Permet d'accéder à la mise en forme de la police du caractère d'ancrage de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [Id](../../aspose.words/comment/id) { get; } | Obtient l'identifiant du commentaire. |
| [Initial](../../aspose.words/comment/initial) { get; set; } | Renvoie ou définit les initiales de l'utilisateur associé à un commentaire spécifique. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/comment/nodetype) { get; } | Retours **NodeType.Comment** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Récupère le parent[`Paragraph`](../paragraph) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [Replies](../../aspose.words/comment/replies) { get; } | Renvoie une collection de[`Comment`](../comment) objets qui sont des enfants immédiats du commentaire spécifié. |
| override [StoryType](../../aspose.words/comment/storytype) { get; } | Retours **StoryType.Comments** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept)(DocumentVisitor) | Accepte un visiteur. |
| [AddReply](../../aspose.words/comment/addreply)(string, string, DateTime, string) | Ajoute une réponse à ce commentaire. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies)() | Supprime toutes les réponses à ce commentaire. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveReply](../../aspose.words/comment/removereply)(Comment) | Supprime la réponse spécifiée à ce commentaire. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [SetText](../../aspose.words/comment/settext)(string) | Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Un commentaire est une annotation ancrée à une zone de texte ou à une position dans le texte. Un commentaire peut contenir une quantité arbitraire de contenu au niveau du bloc.

Si un[`Comment`](../comment) objet se produit tout seul, le commentaire est ancré à la position du[`Comment`](../comment) objet.

Pour ancrer un commentaire à une zone de texte, trois objets sont nécessaires :[`Comment`](../comment) , [`CommentRangeStart`](../commentrangestart) et[`CommentRangeEnd`](../commentrangeend) Les trois objets doivent partager le même [`Id`](./id) évaluer.

[`Comment`](../comment) est un nœud de niveau en ligne et ne peut être qu'un enfant de[`Paragraph`](../paragraph).

[`Comment`](../comment) peut contenir[`Paragraph`](../paragraph) et[`Table`](../../aspose.words.tables/table) nœuds enfants.

### Exemples

Montre comment ajouter un commentaire à un paragraphe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// Dans Microsoft Word, nous pouvons cliquer avec le bouton droit sur ce commentaire dans le corps du document pour le modifier ou y répondre. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Montre comment ajouter un commentaire à un document, puis y répondre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Place le commentaire à un nœud dans le corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge de droite de la page, et avec une ligne pointillée la reliant à son paragraphe.
builder.CurrentParagraph.AppendChild(comment);

// Ajouter une réponse, qui apparaîtra sous son commentaire parent.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Les commentaires et les réponses sont tous deux des nœuds de commentaire.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Les commentaires qui ne répondent pas aux autres commentaires sont "de niveau supérieur". Ils n'ont pas de commentaires d'ancêtre.
Assert.Null(comment.Ancestor);

// Les réponses ont un commentaire de niveau supérieur ancêtre.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Voir également

* class [InlineStory](../inlinestory)
* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
