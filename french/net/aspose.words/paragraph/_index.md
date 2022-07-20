---
title: Paragraph
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente un paragraphe de texte.
type: docs
weight: 4150
url: /fr/net/aspose.words/paragraph/
---
## Paragraph class

Représente un paragraphe de texte.

```csharp
public class Paragraph : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Paragraph](paragraph)(DocumentBase) | Initialise une nouvelle instance du **Paragraphe** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator) { get; } | Vrai si ce saut de paragraphe est un séparateur de style. Un séparateur de style permet à un paragraphe de se composer de parties qui ont différents styles de paragraphe. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtient le document auquel ce nœud appartient. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtient le premier enfant du nœud. |
| [FrameFormat](../../aspose.words/paragraph/frameformat) { get; } | Donne accès aux propriétés de formatage des paragraphes. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell) { get; } | Vrai si ce paragraphe est le dernier paragraphe d'un[`Cell`](../../aspose.words.tables/cell) ; faux sinon. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument) { get; } | Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter) { get; } | Vrai si ce paragraphe est le dernier paragraphe de la **En-têtePied de page** (histoire du texte principal) d'un **Section** ; faux sinon. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection) { get; } | Vrai si ce paragraphe est le dernier paragraphe de la **Corps** (histoire du texte principal) d'un **Section** ; faux sinon. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInCell](../../aspose.words/paragraph/isincell) { get; } | Vrai si ce paragraphe est un enfant immédiat de[`Cell`](../../aspose.words.tables/cell) ; faux sinon. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsListItem](../../aspose.words/paragraph/islistitem) { get; } | Vrai lorsque le paragraphe est un élément d'une liste à puces ou numérotée dans la révision d'origine. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [ListFormat](../../aspose.words/paragraph/listformat) { get; } | Permet d'accéder aux propriétés de formatage de la liste du paragraphe. |
| [ListLabel](../../aspose.words/paragraph/listlabel) { get; } | Obtient un[`ListLabel`](./listlabel) objet qui donne accès à la valeur de numérotation de la liste et au formatage pour ce paragraphe. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/paragraph/nodetype) { get; } | Retours **NodeType.Paragraph** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont) { get; } | Permet d'accéder à la mise en forme de la police du caractère de saut de paragraphe. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat) { get; } | Donne accès aux propriétés de formatage des paragraphes. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentSection](../../aspose.words/paragraph/parentsection) { get; } | Récupère le parent[`Section`](../section) du paragraphe. |
| [ParentStory](../../aspose.words/paragraph/parentstory) { get; } | Récupère l'histoire au niveau de la section parent qui peut être[`Body`](../body) ou[`HeaderFooter`](../headerfooter) . |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [Runs](../../aspose.words/paragraph/runs) { get; } | Fournit un accès à la collection typée de morceaux de texte à l'intérieur du paragraphe. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_1)(string) | Ajoute un champ à ce paragraphe. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield)(FieldType, bool) | Ajoute un champ à ce paragraphe. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_2)(string, string) | Ajoute un champ à ce paragraphe. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops)() | Renvoie un tableau de tous les taquets de tabulation appliqués à ce paragraphe, y compris appliqués indirectement par des styles ou des listes. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/paragraph/gettext)() | Obtient le texte de ce paragraphe, y compris le caractère de fin de paragraphe. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_1)(string, Node, bool) | Insère un champ dans ce paragraphe. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield)(FieldType, bool, Node, bool) | Insère un champ dans ce paragraphe. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_2)(string, string, Node, bool) | Insère un champ dans ce paragraphe. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting)() | Les jointures s'exécutent avec le même formatage dans le paragraphe. |
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

[`Paragraph`](../paragraph) est un nœud de niveau bloc et peut être un enfant de classes dérivées de [`Story`](../story) ou[`InlineStory`](../inlinestory).

[`Paragraph`](../paragraph) peut contenir n'importe quel nombre de nœuds et de signets de niveau en ligne.

La liste complète des nœuds enfants pouvant apparaître à l'intérieur d'un paragraphe se compose de [`BookmarkStart`](../bookmarkstart) ,[`BookmarkEnd`](../bookmarkend) , [`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) , [`FieldEnd`](../../aspose.words.fields/fieldend) ,[`FormField`](../../aspose.words.fields/formfield) , [`Comment`](../comment) ,[`Footnote`](../../aspose.words.notes/footnote) , [`Run`](../run) ,[`SpecialChar`](../specialchar) , [`Shape`](../../aspose.words.drawing/shape) ,[`GroupShape`](../../aspose.words.drawing/groupshape) , [`SmartTag`](../../aspose.words.markup/smarttag).

Un paragraphe valide dans Microsoft Word se termine toujours par un caractère de saut de paragraphe et un paragraphe valide minimal se compose uniquement d'un saut de paragraphe. La **Paragraphe** La classe ajoute automatiquement le caractère de saut de paragraphe approprié à la fin et ce caractère ne fait pas partie des nœuds enfants de la **Paragraphe** , donc a **Paragraphe** peut être vide.

Ne pas inclure la fin du paragraphe[`ControlChar.ParagraphBreakControlChar.ParagraphBreak`](../controlchar/paragraphbreak) ou fin de cellule[`ControlChar.Cell`](../controlchar/cell) caractères à l'intérieur du texte of le paragraphe car cela pourrait rendre le paragraphe invalide lorsque le document est ouvert dans Microsoft Word.

### Exemples

Montre comment construire un document Aspose.Words à la main.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et se retrouver avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a plus de nœuds enfants composites auxquels nous pouvons ajouter du contenu.
// Si nous souhaitons l'éditer, nous devrons repeupler sa collection de nœuds.
// Tout d'abord, créez une nouvelle section, puis ajoutez-la en tant qu'enfant au nœud de document racine.
Section section = new Section(doc);
doc.AppendChild(section);

// Définit certaines propriétés de mise en page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Crée un paragraphe, définit certaines propriétés de formatage, puis l'ajoute en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour faire le document. Créer une course,
// définit son apparence et son contenu, puis l'ajoute en tant qu'enfant au paragraphe.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Voir également

* class [CompositeNode](../compositenode)
* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
