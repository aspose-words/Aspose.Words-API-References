---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.HeaderFooter, votre solution pour gérer facilement les en-têtes et pieds de section. Améliorez la mise en forme de vos documents dès aujourd'hui !
type: docs
weight: 3530
url: /fr/net/aspose.words/headerfooter/
---
## HeaderFooter class

Représente un conteneur pour le texte d'en-tête ou de pied de page d'une section.

Pour en savoir plus, visitez le[Travailler avec les en-têtes et les pieds de page](https://docs.aspose.com/words/net/working-with-headers-and-footers/) article de documentation.

```csharp
public class HeaderFooter : Story
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | Crée un nouvel en-tête ou pied de page du type spécifié. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Obtient le premier paragraphe de l'histoire. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Obtient le type de cet en-tête/pied de page. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Vrai si ceci`HeaderFooter` l'objet est un en-tête. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Vrai si cet en-tête ou pied de page est lié à l'en-tête ou pied de page correspondant dans la section précédente. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Obtient le dernier paragraphe de l'histoire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | RetoursHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont les enfants immédiats de l'histoire. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Obtient la section parent de cette histoire. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Obtient le type de cette histoire. |
| [Tables](../../aspose.words/story/tables/) { get; } | Obtient une collection de tables qui sont les enfants immédiats de l'histoire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour avoir visité la fin de l'en-tête. |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour visiter le début de l'en-tête. |
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

`HeaderFooter` peut contenir[`Paragraph`](../paragraph/) et[`Tableau`](../../aspose.words.tables/table/) nœuds enfants.

`HeaderFooter` est un nœud de niveau section et ne peut être qu'un enfant de[`Section`](../section/) . Il ne peut y en avoir qu'un`HeaderFooter` de chaque[`HeaderFooterType`](./headerfootertype/) dans un[`Section`](../section/).

Si[`Section`](../section/) n'a pas de`HeaderFooter` d'un type spécifique ou le`HeaderFooter` n'a pas de nœuds enfants, cet en-tête/pied de page est considéré comme lié à l'en-tête/pied de page du même type de la section précédente dans Microsoft Word.

Quand`HeaderFooter` contient au moins un[`Paragraph`](../paragraph/), il n'est plus considéré comme lié au précédent dans Microsoft Word.

## Exemples

Montre comment remplacer du texte dans le pied de page d'un document.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Montre comment supprimer tous les pieds de page d'un document.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Parcourez chaque section et supprimez les pieds de page de toutes sortes.
foreach (Section section in doc.OfType<Section>())
{
    // Il existe trois types de pieds de page et d'en-têtes.
    // 1 - L'en-tête/pied de page « Premier », qui n'apparaît que sur la première page d'une section.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - L'en-tête/pied de page « Principal », qui apparaît sur les pages impaires.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - L'en-tête/pied de page « Pair », qui apparaît sur les pages paires.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Montre comment créer un en-tête et un pied de page.

```csharp
Document doc = new Document();

// Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du texte principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra au bas de chaque page de cette section, sous le texte principal.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Voir également

* class [Story](../story/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
