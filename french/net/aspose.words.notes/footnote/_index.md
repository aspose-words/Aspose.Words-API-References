---
title: Footnote
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente un conteneur pour le texte dune note de bas de page ou dune note de fin.
type: docs
weight: 4020
url: /fr/net/aspose.words.notes/footnote/
---
## Footnote class

Représente un conteneur pour le texte d'une note de bas de page ou d'une note de fin.

```csharp
public class Footnote : InlineStory
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Footnote](footnote)(DocumentBase, FootnoteType) | Initialise une instance du **note de bas de page** classe. |

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
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype) { get; } | Renvoie une valeur qui spécifie s'il s'agit d'une note de bas de page ou d'une note de fin. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [IsAuto](../../aspose.words.notes/footnote/isauto) { get; set; } | Contient une valeur qui spécifie s'il s'agit d'une note de bas de page numérotée automatiquement ou d'une note de bas de page avec une marque de référence personnalisée définie par l'utilisateur. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype) { get; } | Retours **NodeType.FootnoteNodeType.Footnote** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark) { get; set; } | Obtient/définit la marque de référence personnalisée à utiliser pour cette note de bas de page. La valeur par défaut est **chaîne vide** (Empty ), ce qui signifie que des notes de bas de page numérotées automatiquement sont utilisées. |
| override [StoryType](../../aspose.words.notes/footnote/storytype) { get; } | Retours **StoryType.Footnotes** ou **StoryType.Endnotes** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype) . |
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

La **note de bas de page** La classe est utilisée pour représenter à la fois les notes de bas de page et les notes de fin dans un document Word.

**note de bas de page** est un nœud de niveau en ligne et ne peut être qu'un enfant de **Paragraphe**.

**note de bas de page** peut contenir **Paragraphe** et **Table** nœuds enfants.

### Exemples

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

* class [InlineStory](../../aspose.words/inlinestory)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
