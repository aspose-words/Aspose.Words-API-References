---
title: InlineStory
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de base pour les nœuds de niveau en ligne pouvant contenir des paragraphes et des tableaux.
type: docs
weight: 3070
url: /fr/net/aspose.words/inlinestory/
---
## InlineStory class

Classe de base pour les nœuds de niveau en ligne pouvant contenir des paragraphes et des tableaux.

```csharp
public abstract class InlineStory : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtient le document auquel ce nœud appartient. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Obtient le premier paragraphe de l'histoire. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Permet d'accéder à la mise en forme de la police du caractère d'ancrage de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Obtient le type de ce nœud. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Récupère le parent[`Paragraph`](../paragraph) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype) { get; } | Renvoie le type de l'histoire. |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Accepte un visiteur. |
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
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

**InlineStory** est un conteneur pour les nœuds de niveau bloc[`Paragraph`](../paragraph) et[`Table`](../../aspose.words.tables/table).

Les classes qui dérivent de **InlineStory** sont des nœuds de niveau ligne qui peuvent contenir leur propre texte (paragraphes et tableaux). Par exemple, un **Commentaire** nœud contient le texte d'un commentaire et d'un **note de bas de page** contient le texte d'une note de bas de page.

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
// marquer après le texte auquel il fait référence et créer une entrée sous le corps du texte principal au bas de la page.
// Cette entrée contiendra la marque de référence de la note de bas de page et le texte de référence,
// que nous transmettrons à la méthode "InsertFootnote" du générateur de document.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si cette propriété vaut "true", alors le repère de notre note de bas de page
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

// Un signet avec le drapeau "IsAuto" défini sur true affichera toujours son index réel
// même si les signets précédents affichent des marques de référence personnalisées, la marque de référence de ce signet sera donc un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Voir également

* class [CompositeNode](../compositenode)
* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
