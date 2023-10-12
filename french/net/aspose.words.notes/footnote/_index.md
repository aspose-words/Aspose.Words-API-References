---
title: Class Footnote
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Notes.Footnote classe. Représente un conteneur pour le texte dune note de bas de page ou dune note de fin.
type: docs
weight: 4260
url: /fr/net/aspose.words.notes/footnote/
---
## Footnote class

Représente un conteneur pour le texte d'une note de bas de page ou d'une note de fin.

Pour en savoir plus, visitez le[Travailler avec les notes de bas de page et de fin](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) article documentaire.

```csharp
public class Footnote : InlineStory
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Footnote](footnote/)(DocumentBase, FootnoteType) | Initialise une instance du`Footnote` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Obtient le premier paragraphe de l'histoire. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Donne accès au formatage de la police du caractère d'ancrage de cet objet. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Renvoie une valeur qui spécifie s'il s'agit d'une note de bas de page ou d'une note de fin. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Contient une valeur qui spécifie s'il s'agit d'une note de bas de page numérotée automatiquement ou d'une note de bas de page avec une marque de référence personnalisée définie par l'utilisateur. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | RetoursFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont des enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Obtient/définit la marque de référence personnalisée à utiliser pour cette note de bas de page. La valeur par défaut est **chaîne vide** (Empty ), ce qui signifie que des notes de bas de page numérotées automatiquement sont utilisées. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | RetoursFootnotes ouEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Obtient une collection de tables qui sont des enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(DocumentVisitor) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
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
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

### Remarques

Le`Footnote` La classe est utilisée pour représenter à la fois les notes de bas de page et les notes de fin dans un document Word.

`Footnote` est un nœud de niveau en ligne et ne peut être qu'un enfant de[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` peut contenir[`Paragraph`](../../aspose.words/paragraph/) et[`Table`](../../aspose.words.tables/table/) nœuds enfants.

### Exemples

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

* class [InlineStory](../../aspose.words/inlinestory/)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)


