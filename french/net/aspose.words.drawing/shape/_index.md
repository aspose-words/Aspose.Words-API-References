---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Shape classe. Représente un objet dans le calque de dessin tel quune forme automatique une zone de texte une forme libre un objet OLE un contrôle ActiveX ou une image en C#.
type: docs
weight: 1250
url: /fr/net/aspose.words.drawing/shape/
---
## Shape class

Représente un objet dans le calque de dessin, tel qu'une forme automatique, une zone de texte, une forme libre, un objet OLE, un contrôle ActiveX ou une image.

Pour en savoir plus, visitez le[Travailler avec des formes](https://docs.aspose.com/words/net/working-with-shapes/) article documentaire.

```csharp
public sealed class Shape : ShapeBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Crée un nouvel objet de forme. |

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
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Donne accès aux propriétés du graphique si cette forme a un[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Les coordonnées dans le coin supérieur gauche du bloc contenant cette forme. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc contenant cette forme. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord droit de la forme. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Retours`vrai` si un effet d'extrusion est activé. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Obtient le formatage de remplissage pour la forme. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Définit la couleur du pinceau qui remplit le chemin fermé de la forme. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Détermine si le chemin fermé de la forme sera rempli. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Obtient le premier paragraphe de la forme. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Change l'orientation d'une forme. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Donne accès au formatage de la police de cet objet. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Retours`vrai` si ce`Shape` a un[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Retours`vrai` si la forme contient des octets d'image ou lie une image. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Retours`vrai` si ce`Shape` a un objet SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtient ou définit la hauteur du bloc contenant la forme. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Obtient ou définit la valeur qui représente le pourcentage de la hauteur relative de la forme. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Spécifie comment la forme est positionnée horizontalement. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Donne accès aux propriétés de la forme de règle horizontale. Pour une forme qui n'est pas une règle horizontale, renvoie`nul` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Obtient ou définit l'adresse complète du lien hypertexte pour une forme. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Donne accès à l'image de la forme. `nul` si la forme ne peut pas avoir d'image. |
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
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Obtient le dernier paragraphe de la forme. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtient ou définit la position du bord gauche du bloc contenant la forme. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Obtient ou définit la valeur qui représente la position relative à gauche de la forme en pourcentage. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Obtient le MarkupLanguage utilisé pour cet objet graphique. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtient ou définit le nom de la forme facultatif. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | RetoursShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Fournit un accès aux données OLE d'une forme. Pour une forme qui n'est pas un objet OLE ou un contrôle ActiveX, renvoie`nul` . |
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
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Retours`vrai` si un effet d'ombre est activé. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtient le formatage de l'ombre pour la forme. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtient le type de forme. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Obtient[`SignatureLine`](../signatureline/) objet si la forme est une ligne de signature. Retour`nul` sinon. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtient la taille de la forme en points. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | RetoursTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Définit un trait pour une forme. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Définit la couleur d'un trait. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Définit si le chemin sera tracé. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtient ou définit le cadre cible pour le lien hypertexte de forme. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Définit les attributs qui spécifient la façon dont le texte est affiché dans une forme. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Définit le texte du chemin de texte (d'un objet WordArt). |
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
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Ajoute au rectangle source les valeurs de l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un duplicata du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crée et renvoie un objet qui peut être utilisé pour restituer cette forme en image. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Convertit une valeur de l'espace de coordonnées local dans l'espace de coordonnées de la forme parent. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Supprime le nœud enfant spécifié. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Réservé à l'utilisation du système. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Met à jour le dessin pré-rendu SmartArt à l'aide du moteur de rendu à froid SmartArt d'Aspose.Words. |

## Remarques

En utilisant le`Shape` classe, vous pouvez créer ou modifier des formes dans un document Microsoft Word.

Une propriété importante d'une forme est sa[`ShapeType`](../shapebase/shapetype/)Les formes de types different peuvent avoir différentes fonctionnalités dans un document Word. Par exemple, seuls image et OLE shape peuvent contenir des images. La plupart des formes peuvent contenir du texte, mais pas toutes.

Les formes pouvant contenir du texte peuvent contenir[`Paragraph`](../../aspose.words/paragraph/) et [`Table`](../../aspose.words.tables/table/) nœuds comme enfants.

## Exemples

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

Montre comment extraire des images d'un document et les enregistrer sur le système de fichiers local en tant que fichiers individuels.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Récupère la collection de formes du document,
// et enregistrez les données d'image de chaque forme avec une image sous forme de fichier dans le système de fichiers local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Les données d'image des formes peuvent contenir des images de nombreux formats d'image possibles.
        // Nous pouvons déterminer automatiquement une extension de fichier pour chaque image, en fonction de son format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Montre comment supprimer toutes les formes d’un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère deux formes avec une forme de groupe contenant une autre forme à l'intérieur.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// Supprime tous les nœuds Shape du document.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Toutes les formes ont disparu, mais la forme de groupe est toujours dans le document.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Supprime toutes les formes de groupe séparément.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* class [ShapeBase](../shapebase/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
