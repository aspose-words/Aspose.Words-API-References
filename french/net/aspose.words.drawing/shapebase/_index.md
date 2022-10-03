---
title: ShapeBase
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de base pour les objets de la couche de dessin tels quune forme automatique une forme libre un objet OLE un contrôle ActiveX ou une image.
type: docs
weight: 1110
url: /fr/net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Classe de base pour les objets de la couche de dessin, tels qu'une forme automatique, une forme libre, un objet OLE, un contrôle ActiveX ou une image.

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
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Spécifie si la forme est au-dessous ou au-dessus du texte. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Obtient la position du bord inférieur du bloc conteneur de la forme. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Obtient ou définit l'emplacement et la taille du bloc conteneur de la forme. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Obtient l'emplacement et la taille du bloc conteneur de la forme en points, par rapport à l'ancre de la forme la plus haute. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Obtient l'étendue finale de cet objet de forme après l'application des effets de dessin. La valeur est mesurée en points. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Renvoie vrai si le type de forme permet à la forme d'avoir une image. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Les coordonnées dans le coin supérieur gauche du bloc conteneur de cette forme. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc conteneur de cette forme. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord droit de la forme. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Obtient la mise en forme de remplissage pour la forme. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Change l'orientation d'une forme. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Fournit l'accès à la mise en forme de la police de cet objet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtient ou définit la hauteur du bloc conteneur de la forme. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Spécifie comment la forme est positionnée horizontalement. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Obtient ou définit l'adresse complète du lien hypertexte pour une forme. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Obtient ou définit l'indicateur qui spécifie si la forme est décorative dans le document. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Renvoie vrai s'il s'agit d'une forme de groupe. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Renvoie vrai si cette forme est une règle horizontale. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Renvoie vrai si cette forme est une forme d'image. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Un moyen rapide de déterminer si cette forme est alignée avec le texte. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Obtient ou définit un indicateur indiquant si la forme est affichée à l'intérieur ou à l'extérieur d'un tableau. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indique que la forme est une SignatureLine. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Renvoie vrai si cette forme n'est pas un enfant d'une forme de groupe. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Renvoie true si cette forme est un objet WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtient ou définit la position du bord gauche du bloc conteneur de la forme. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Récupère MarkupLanguage utilisé pour cet objet graphique. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtient ou définit le nom de la forme facultative. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Renvoie le paragraphe parent immédiat. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée horizontalement. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Spécifie par rapport à quoi la forme est positionnée verticalement. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Obtient la position du bord droit du bloc conteneur de la forme. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Définit l'angle (en degrés) de rotation d'une forme. Une valeur positive correspond à un angle de rotation dans le sens des aiguilles d'une montre. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtient la mise en forme de l'ombre pour la forme. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtient le type de forme. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtient la taille de la forme en points. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtient ou définit le cadre cible pour le lien hypertexte de la forme. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Obtient ou définit le titre (légende) de l'objet forme actuel. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Obtient ou définit la position du bord supérieur du bloc conteneur de la forme. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Spécifie comment la forme est positionnée verticalement. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Obtient ou définit la largeur du bloc conteneur de la forme. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Spécifie comment le texte est enroulé autour de la forme. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Détermine l'ordre d'affichage des formes superposées. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Ajoute aux valeurs du rectangle source de l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crée et renvoie un objet qui peut être utilisé pour rendre cette forme dans une image. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Convertit une valeur de l'espace de coordonnées local dans l'espace de coordonnées de la forme parent. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Ceci est une classe abstraite. Les deux classes dérivées que vous pouvez instancier sont[`Shape`](../shape/) et[`GroupShape`](../groupshape/).

Une forme est un nœud dans l'arborescence du document.

Si la forme est un enfant d'un[`Paragraph`](../../aspose.words/paragraph/) objet, alors la forme est dite "de niveau supérieur". Les formes de niveau supérieur sont mesurées et positionnées en points.

Une forme peut également apparaître en tant qu'enfant d'un[`GroupShape`](../groupshape/) objet lorsque plusieurs formes sont regroupées. Les formes enfant d'une forme de groupe sont positionnées dans l'espace de coordonnées et units défini par le[`CoordSize`](./coordsize/) et[`CoordOrigin`](./coordorigin/)propriétés de la forme de groupe parent .

Une forme peut être alignée avec du texte ou flottante. La méthode de positionnement est contrôlée à l'aide de la[`WrapType`](./wraptype/) propriété.

Lorsqu'une forme est flottante, elle est positionnée par rapport à quelque chose (par exemple le paragraphe courant, la marge ou la page). Le positionnement relatif de la forme est spécifié à l'aide de the [`RelativeHorizontalPosition`](./relativehorizontalposition/) et[`RelativeVerticalPosition`](./relativeverticalposition/) Propriétés.

Une forme flottante doit être positionnée explicitement à l'aide de la[`Left`](./left/) et[`Top`](./top/) propriétés ou aligné par rapport à un autre objet à l'aide de la[`HorizontalAlignment`](./horizontalalignment/) et[`VerticalAlignment`](./verticalalignment/) Propriétés.

### Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et l'aligne au centre de la page.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
