---
title: Class ShapeBase
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.ShapeBase classe. Classe de base pour les objets du calque de dessin tels quune forme automatique une forme libre un objet OLE un contrôle ActiveX ou une image.
type: docs
weight: 1260
url: /fr/net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Classe de base pour les objets du calque de dessin, tels qu'une forme automatique, une forme libre, un objet OLE, un contrôle ActiveX ou une image.

Pour en savoir plus, visitez le[Travailler avec des formes](https://docs.aspose.com/words/net/working-with-shapes/) article documentaire.

```csharp
public abstract class ShapeBase : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Obtient ou définit une valeur qui spécifie si cette forme peut chevaucher d'autres formes. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Définit un texte alternatif à afficher à la place d'un graphique. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Spécifie si l'ancre de la forme est verrouillée. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Spécifie si les proportions de la forme sont verrouillées. |
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
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Donne accès au formatage de la police de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtient ou définit la hauteur du bloc contenant la forme. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Obtient ou définit la valeur qui représente le pourcentage de la hauteur relative de la forme. |
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
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Retours`vrai`si cette forme n'est pas un enfant d'une forme de groupe. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Retours`vrai` si cette forme est un objet WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtient ou définit la position du bord gauche du bloc contenant la forme. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Obtient ou définit la valeur qui représente la position relative à gauche de la forme en pourcentage. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Obtient le MarkupLanguage utilisé pour cet objet graphique. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtient ou définit le nom de la forme facultatif. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Renvoie le paragraphe parent immédiat. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée horizontalement. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Obtient ou définit la valeur de la taille relative de la forme dans la direction horizontale. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée verticalement. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Obtient ou définit la valeur de la taille relative de la forme dans la direction verticale. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Obtient la position du bord droit du bloc contenant la forme. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Définit l'angle (en degrés) de rotation d'une forme. La valeur positive correspond à l'angle de rotation dans le sens des aiguilles d'une montre. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtient le formatage de l'ombre pour la forme. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtient le type de forme. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtient la taille de la forme en points. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtient ou définit le cadre cible pour le lien hypertexte de forme. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Obtient ou définit le titre (légende) de l'objet de forme actuel. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Obtient ou définit la position du bord supérieur du bloc contenant la forme. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Obtient ou définit la valeur qui représente la position supérieure relative de la forme en pourcentage. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Spécifie comment la forme est positionnée verticalement. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Obtient ou définit la largeur du bloc contenant la forme. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Spécifie comment le texte est enroulé autour de la forme. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Détermine l'ordre d'affichage des formes qui se chevauchent. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepte un visiteur. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(DocumentVisitor) |  |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(DocumentVisitor) |  |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Ajoute au rectangle source les valeurs de l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crée et renvoie un objet qui peut être utilisé pour restituer cette forme en image. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Convertit une valeur de l'espace de coordonnées local dans l'espace de coordonnées de la forme parent. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

### Remarques

Il s'agit d'une classe abstraite. Les deux classes dérivées que vous pouvez instancier sont[`Shape`](../shape/) et[`GroupShape`](../groupshape/).

Une forme est un nœud dans l'arborescence du document.

Si la forme est l'enfant d'un[`Paragraph`](../../aspose.words/paragraph/) objet, alors la forme est dite "de niveau supérieur". Les formes de niveau supérieur sont mesurées et positionnées en points.

Une forme peut également apparaître en tant qu'enfant d'un[`GroupShape`](../groupshape/) objet lorsque plusieurs formes sont regroupées. Les formes enfants d'une forme de groupe sont positionnées dans l'espace de coordonnées et les unités définies par le[`CoordSize`](./coordsize/) et[`CoordOrigin`](./coordorigin/) propriétés de la forme du groupe parent .

Une forme peut être positionnée en ligne avec le texte ou flottante. La méthode de positionnement est contrôlée à l'aide du[`WrapType`](./wraptype/) propriété.

Lorsqu'une forme est flottante, elle est positionnée par rapport à quelque chose (par exemple le paragraphe courant, la marge ou la page). Le positionnement relatif de la forme est spécifié à l'aide de the [`RelativeHorizontalPosition`](./relativehorizontalposition/) et[`RelativeVerticalPosition`](./relativeverticalposition/) propriétés.

Une forme flottante doit être positionnée explicitement à l'aide du[`Left`](./left/) et[`Top`](./top/) propriétés ou alignés par rapport à un autre objet à l'aide du[`HorizontalAlignment`](./horizontalalignment/) et[`VerticalAlignment`](./verticalalignment/) propriétés.

### Exemples

Montre comment insérer une image flottante au centre d’une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Voir également

* class [CompositeNode](../../aspose.words/compositenode/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


