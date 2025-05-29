---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Paragraph pour gérer et formater sans effort des paragraphes de texte, améliorant ainsi vos capacités de traitement de documents.
type: docs
weight: 5120
url: /fr/net/aspose.words/paragraph/
---
## Paragraph class

Représente un paragraphe de texte.

Pour en savoir plus, visitez le[Travailler avec des paragraphes](https://docs.aspose.com/words/net/working-with-paragraphs/) article de documentation.

```csharp
public class Paragraph : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Initialise une nouvelle instance du`Paragraph` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Vrai si ce saut de paragraphe est un séparateur de style. Un séparateur de style permet à un paragraphe de se composer de parties ayant des styles de paragraphe différents. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Donne accès aux propriétés de formatage du cadre. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Vrai si ce paragraphe est le dernier paragraphe d'un[`Cell`](../../aspose.words.tables/cell/) ; faux sinon. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Vrai si ce paragraphe est le dernier paragraphe du[`HeaderFooter`](../headerfooter/) (histoire du texte principal) d'un[`Section`](../section/) ; faux sinon. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Vrai si ce paragraphe est le dernier paragraphe du[`Body`](../body/) (histoire du texte principal) d'un[`Section`](../section/) ; faux sinon. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Vrai si ce paragraphe est un enfant immédiat de[`Cell`](../../aspose.words.tables/cell/) ; faux sinon. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Vrai lorsque le paragraphe est un élément d'une liste à puces ou numérotée dans la révision d'origine. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Donne accès aux propriétés de formatage de la liste du paragraphe. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Obtient un[`ListLabel`](./listlabel/)objet qui donne accès à la valeur de numérotation de liste et au formatage pour ce paragraphe. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | RetoursParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Donne accès à la mise en forme de la police du caractère de saut de paragraphe. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Donne accès aux propriétés de formatage des paragraphes. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Récupère le parent[`Section`](../section/) du paragraphe. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Récupère l'histoire au niveau de la section parent qui peut être[`Body`](../body/) ou[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Donne accès à la collection tapée de morceaux de texte à l'intérieur du paragraphe. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour visiter la fin du paragraphe du document. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour visiter le début du paragraphe du document. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Ajoute un champ à ce paragraphe. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Ajoute un champ à ce paragraphe. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Ajoute un champ à ce paragraphe. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Renvoie un tableau de tous les taquets de tabulation appliqués à ce paragraphe, y compris ceux appliqués indirectement par des styles ou des listes. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Obtient le texte de ce paragraphe, y compris le caractère de fin de paragraphe. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Insère un champ dans ce paragraphe. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Insère un champ dans ce paragraphe. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Insère un champ dans ce paragraphe. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Les jointures s'exécutent avec le même formatage dans le paragraphe. |
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

`Paragraph` est un nœud de niveau bloc et peut être un enfant de classes dérivées de [`Story`](../story/) ou[`InlineStory`](../inlinestory/).

`Paragraph` peut contenir n'importe quel nombre de nœuds et de signets de niveau en ligne.

La liste complète des nœuds enfants qui peuvent apparaître dans un paragraphe se compose de [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Un paragraphe valide dans Microsoft Word se termine toujours par un caractère de saut de paragraphe et un paragraphe valide minimal se compose simplement d'un saut de paragraphe.`Paragraph` La classe ajoute automatiquement le caractère de saut de paragraphe approprié à la fin et ce caractère ne fait pas partie des nœuds enfants de la`Paragraph` , donc a`Paragraph` peut être vide.

Ne pas inclure la fin du paragraphe[`ParagraphBreak`](../controlchar/paragraphbreak/) ou fin de cellule[`Cell`](../controlchar/cell/) caractères à l'intérieur du texte de le paragraphe car cela pourrait rendre le paragraphe invalide lorsque le document est ouvert dans Microsoft Word.

## Exemples

Montre comment construire un document Aspose.Words à la main.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode « RemoveAllChildren » pour supprimer tous ces nœuds,
// et se retrouver avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a désormais aucun nœud enfant composite auquel nous pouvons ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons repeupler sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
Section section = new Section(doc);
doc.AppendChild(section);

// Définissez certaines propriétés de configuration de page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Créez un paragraphe, définissez certaines propriétés de formatage, puis ajoutez-le en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour compléter le document. Créez une exécution,
// définissez son apparence et son contenu, puis ajoutez-le en tant qu'enfant au paragraphe.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Voir également

* class [CompositeNode](../compositenode/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
