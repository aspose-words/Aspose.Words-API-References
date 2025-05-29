---
title: GroupShape Class
linktitle: GroupShape
articleTitle: GroupShape
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.GroupShape pour gérer et manipuler facilement des formes groupées dans vos documents pour un attrait visuel amélioré.
type: docs
weight: 1350
url: /fr/net/aspose.words.drawing/groupshape/
---
## GroupShape class

Représente un groupe de formes dans un document.

Pour en savoir plus, visitez le[Comment ajouter une forme de groupe dans un document Word](https://docs.aspose.com/words/net/how-to-add-group-shape-into-a-word-document/) article de documentation.

```csharp
public class GroupShape : ShapeBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [GroupShape](groupshape/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Crée une nouvelle forme de groupe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Obtient ou définit une valeur qui spécifie si cette forme peut chevaucher d'autres formes. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Définit un texte alternatif à afficher à la place d'un graphique. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Spécifie si l'ancre de la forme est verrouillée. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Spécifie si le rapport hauteur/largeur de la forme est verrouillé. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Spécifie si la forme est en dessous ou au-dessus du texte. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Obtient la position du bord inférieur du bloc contenant la forme. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Obtient ou définit l'emplacement et la taille du bloc contenant la forme. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Obtient l'emplacement et la taille du bloc contenant la forme en points, par rapport à l'ancre de la forme la plus haute. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Obtient l'étendue finale de cet objet de forme après l'application des effets de dessin. La valeur est mesurée en points. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Retours`vrai` si le type de forme permet à la forme d'avoir une image. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Les coordonnées dans le coin supérieur gauche du bloc contenant cette forme. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc contenant cette forme. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord droit de la forme. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Obtient le formatage de remplissage pour la forme. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Change l'orientation d'une forme. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Donne accès à la mise en forme de la police de cet objet. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Obtient le formatage de lueur pour la forme. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtient ou définit la hauteur du bloc contenant la forme. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Obtient ou définit la valeur qui représente le pourcentage de la hauteur relative de la forme. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Obtient ou définit une valeur booléenne indiquant si la forme est visible. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Spécifie comment la forme est positionnée horizontalement. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Obtient ou définit l'adresse complète du lien hypertexte pour une forme. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Obtient ou définit l'indicateur qui spécifie si la forme est décorative dans le document. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Retours`vrai` s'il s'agit d'une forme de groupe. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Retours`vrai` si cette forme est une règle horizontale. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Retours`vrai` si cette forme est une forme d'image. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Obtient ou définit un indicateur indiquant si la forme est affichée à l'intérieur ou à l'extérieur d'un tableau. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indique que la forme est un[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Retours`vrai` si cette forme n'est pas un enfant d'une forme de groupe. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Retours`vrai` si cette forme est un objet WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtient ou définit la position du bord gauche du bloc contenant la forme. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Obtient ou définit la valeur qui représente la position relative gauche de la forme en pourcentage. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Obtient le MarkupLanguage utilisé pour cet objet graphique. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtient ou définit le nom de la forme facultative. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | RetoursGroupShape . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Renvoie le paragraphe parent immédiat. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Obtient le formatage de réflexion pour la forme. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée horizontalement. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Obtient ou définit la valeur de la taille relative de la forme dans la direction horizontale. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée verticalement. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Obtient ou définit la valeur de la taille relative de la forme dans la direction verticale. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Obtient la position du bord droit du bloc contenant la forme. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Définit l'angle (en degrés) selon lequel une forme est tournée. Une valeur positive correspond à un angle de rotation dans le sens des aiguilles d'une montre. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtient la mise en forme de l'ombre pour la forme. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtient le type de forme. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtient la taille de la forme en points. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Obtient une mise en forme des bords doux pour la forme. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtient ou définit le cadre cible pour le lien hypertexte de forme. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Obtient ou définit le titre (légende) de l'objet de forme actuel. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Obtient ou définit la position du bord supérieur du bloc contenant la forme. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Obtient ou définit la valeur qui représente la position supérieure relative de la forme en pourcentage. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Spécifie comment la forme est positionnée verticalement. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Obtient ou définit la largeur du bloc contenant la forme. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Spécifie comment le texte est enroulé autour de la forme. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Définit si la forme est linéaire ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Détermine l'ordre d'affichage des formes qui se chevauchent. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.drawing/groupshape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter la fin du GroupShape. |
| override [AcceptStart](../../aspose.words.drawing/groupshape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter le début du GroupShape. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Ajoute au rectangle source les valeurs de l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crée et renvoie un objet qui peut être utilisé pour rendre cette forme dans une image. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Convertit une valeur de l'espace de coordonnées local dans l'espace de coordonnées de la forme parent. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

UN`GroupShape` est un nœud composite et peut avoir[`Shape`](../shape/) et `GroupShape` nœuds comme enfants.

Chaque`GroupShape`définit un nouveau système de coordonnées pour ses formes enfants. Le système de coordonnées est défini à l'aide du[`CoordSize`](../shapebase/coordsize/) et [`CoordOrigin`](../shapebase/coordorigin/) propriétés.

## Exemples

Montre comment créer un groupe de formes et imprimer son contenu à l'aide d'un visiteur de document.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Si vous devez créer des formes « NonPrimitives », telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // Coins supérieurs un arrondi un coupé, Coin unique arrondi, Coins supérieurs arrondis, Coins diagonaux arrondis
    // veuillez utiliser les méthodes DocumentBuilder.InsertShape.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200,
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100,
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Imprime le contenu d'un groupe de formes visité sur la console.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [ShapeBase](../shapebase/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
