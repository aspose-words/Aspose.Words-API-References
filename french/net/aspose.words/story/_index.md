---
title: Story Class
linktitle: Story
articleTitle: Story
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Story, votre outil essentiel pour gérer efficacement les éléments au niveau du bloc comme les paragraphes et les tableaux.
type: docs
weight: 6960
url: /fr/net/aspose.words/story/
---
## Story class

Classe de base pour les éléments contenant des nœuds de niveau bloc[`Paragraph`](../paragraph/) et[`Table`](../../aspose.words.tables/table/) .

Pour en savoir plus, visitez le[Niveaux logiques des nœuds dans un document](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) article de documentation.

```csharp
public abstract class Story : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Obtient le premier paragraphe de l'histoire. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont les enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Obtient le type de cette histoire. |
| [Tables](../../aspose.words/story/tables/) { get; } | Obtient une collection de tables qui sont les enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXEnd du visiteur du document spécifié. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXStart du visiteur du document spécifié. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Une méthode de raccourci qui crée un[`Paragraph`](../paragraph/) objet avec texte facultatif et l'ajoute à la fin de cet objet. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Supprime toutes les formes du texte de cette histoire. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

On dit que le texte d'un document Word est composé de plusieurs histoires. Le texte principal est stocké dans l'histoire de texte principal représentée par[`Body`](../body/) , chaque en-tête et pied de page est stocké dans une histoire séparée représentée par[`HeaderFooter`](../headerfooter/).

## Exemples

Montre comment supprimer toutes les formes d'un nœud.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne.
// qui a un paragraphe parent, qui est un nœud enfant du corps de la première section.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce corps.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* class [CompositeNode](../compositenode/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
