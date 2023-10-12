---
title: Class InlineStory
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.InlineStory classe. Classe de base pour les nœuds de niveau en ligne pouvant contenir des paragraphes et des tableaux.
type: docs
weight: 3270
url: /fr/net/aspose.words/inlinestory/
---
## InlineStory class

Classe de base pour les nœuds de niveau en ligne pouvant contenir des paragraphes et des tableaux.

Pour en savoir plus, visitez le[Niveaux logiques des nœuds dans un document](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) article documentaire.

```csharp
public abstract class InlineStory : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Obtient le premier paragraphe de l'histoire. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Donne accès au formatage de la police du caractère d'ancrage de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | Renvoie le type de l'histoire. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepte un visiteur. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(DocumentVisitor) |  |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(DocumentVisitor) |  |
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
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

### Remarques

`InlineStory` est un conteneur pour les nœuds au niveau du bloc[`Paragraph`](../paragraph/) et[`Table`](../../aspose.words.tables/table/).

Les classes qui en dérivent`InlineStory` sont des nœuds de niveau en ligne qui peuvent contenir leur propre texte (paragraphes et tableaux). Par exemple, un[`Comment`](../comment/) Le nœud contient le texte d'un commentaire et d'un[`Footnote`](../../aspose.words.notes/footnote/) contient le texte d’une note de bas de page.

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

Montre comment insérer et personnaliser des notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte et référencez-le avec une note de bas de page. Cette note de bas de page placera une petite référence en exposant
// marque après le texte auquel il fait référence et crée une entrée sous le corps du texte principal en bas de la page.
// Cette entrée contiendra la marque de référence de la note de bas de page et le texte de référence,
// que nous transmettrons à la méthode "InsertFootnote" du générateur de documents.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si cette propriété est définie sur "true", alors la marque de référence de notre note de bas de page
// sera son index parmi toutes les notes de bas de page de la section.
// Ceci est la première note de bas de page, donc la marque de référence sera "1".
Assert.True(footnote.IsAuto);

 // Nous pouvons déplacer le générateur de document à l'intérieur de la note de bas de page pour modifier son texte de référence.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Nous pouvons définir une marque de référence personnalisée que la note de bas de page utilisera à la place de son numéro d'index.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un signet avec l'indicateur "IsAuto" défini sur true affichera toujours son véritable index
// même si les signets précédents affichent des marques de référence personnalisées, la marque de référence de ce signet sera donc un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Voir également

* class [CompositeNode](../compositenode/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


