---
title: Class Comment
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Comment classe. Représente un conteneur pour le texte dun commentaire.
type: docs
weight: 230
url: /fr/net/aspose.words/comment/
---
## Comment class

Représente un conteneur pour le texte d'un commentaire.

Pour en savoir plus, visitez le[Travailler avec des commentaires](https://docs.aspose.com/words/net/working-with-comments/) article documentaire.

```csharp
public sealed class Comment : InlineStory
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Initialise une nouvelle instance du`Comment` classe. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Initialise une nouvelle instance du`Comment` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Renvoie le parent`Comment` objet. Retour`nul` pour les commentaires de niveau supérieur. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Renvoie ou définit le nom de l'auteur d'un commentaire. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Obtient la date et l'heure auxquelles le commentaire a été fait. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Obtient ou définit l'indicateur indiquant que le commentaire a été marqué comme terminé. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Obtient le premier paragraphe de l'histoire. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Donne accès au formatage de la police du caractère d'ancrage de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Obtient l'identifiant du commentaire. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Renvoie ou définit les initiales de l'utilisateur associé à un commentaire spécifique. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | RetoursComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Renvoie une collection de`Comment` objets qui sont des enfants immédiats du commentaire spécifié. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | RetoursComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(DocumentVisitor) |  |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Ajoute une réponse à ce commentaire. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Supprime toutes les réponses à ce commentaire. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Supprime la réponse spécifiée à ce commentaire. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../node/) qui correspond à l'expression XPath. |
| [SetText](../../aspose.words/comment/settext/)(string) | Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

### Remarques

Un commentaire est une annotation ancrée à une région de texte ou à une position dans le texte. Un commentaire peut contenir une quantité arbitraire de contenu au niveau du bloc.

Si un`Comment` l'objet apparaît tout seul, le commentaire est ancré à la position du`Comment` objet.

Pour ancrer un commentaire à une zone de texte, trois objets sont nécessaires :`Comment` , [`CommentRangeStart`](../commentrangestart/) et[`CommentRangeEnd`](../commentrangeend/) . Les trois objets doivent partager le même [`Id`](./id/) valeur.

`Comment` est un nœud de niveau en ligne et ne peut être qu'un enfant de[`Paragraph`](../paragraph/).

`Comment` peut contenir[`Paragraph`](../paragraph/) et[`Table`](../../aspose.words.tables/table/) nœuds enfants.

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

// Place le commentaire à un nœud du corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge droite de la page, et avec une ligne pointillée la reliant à son paragraphe.
builder.CurrentParagraph.AppendChild(comment);

// Ajoute une réponse, qui apparaîtra sous son commentaire parent.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Les commentaires et les réponses sont tous deux des nœuds de commentaires.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Les commentaires qui ne répondent pas aux autres commentaires sont du "niveau supérieur". Ils n'ont aucun commentaire d'ancêtre.
Assert.Null(comment.Ancestor);

// Les réponses ont un commentaire de niveau supérieur ancêtre.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Voir également

* class [InlineStory](../inlinestory/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


