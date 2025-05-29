---
title: ShapeBase.CoordSize
linktitle: CoordSize
articleTitle: CoordSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase CoordSize, définissant la largeur et la hauteur de l'espace de coordonnées pour un contrôle optimal de la mise en page dans vos projets de conception.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc contenant cette forme.

```csharp
public Size CoordSize { get; set; }
```

## Remarques

La valeur par défaut est (1000, 1000).

## Exemples

Montre comment traduire l'emplacement des coordonnées x et y sur le plan de coordonnées d'une forme vers un emplacement sur le plan de coordonnées de la forme parent.

```csharp
Document doc = new Document();

// Insérez une forme de groupe et placez-la 100 points en dessous et à droite de
// le point d'origine des coordonnées x et Y du document.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Utilisez la méthode « LocalToParent » pour déterminer que (0, 0) sur les coordonnées x et y internes du groupe
// se trouve sur (100, 100) du système de coordonnées de sa forme parente. Le parent de la forme de groupe est le document lui-même.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Par défaut, le plan de coordonnées interne d'une forme a le coin supérieur gauche à (0, 0),
// et le coin inférieur droit à (1000, 1000). De par sa taille, notre forme de groupe couvre une surface de 500 pt x 500 pt.
// dans le plan du document. Cela signifie qu'un déplacement de 1 point sur le plan de coordonnées du document entraînera une translation.
// à un mouvement de 2 points sur le plan de coordonnées de la forme du groupe.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Déplacez l'origine des axes x et y de la forme du groupe du coin supérieur gauche vers le centre.
// Cela décalera encore davantage les coordonnées internes du groupe par rapport aux coordonnées du document.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// La modification de l'échelle du plan de coordonnées affectera également les emplacements relatifs.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Si nous souhaitons ajouter une forme à ce groupe tout en définissant son emplacement en fonction d'un emplacement dans le document,
// nous devrons d'abord confirmer un emplacement dans la forme du groupe qui correspondra à l'emplacement du document.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

Montre comment créer et remplir une forme de groupe.

```csharp
Document doc = new Document();

// Créer une forme de groupe. Une forme de groupe peut afficher une collection de nœuds de forme enfant.
// Dans Microsoft Word, cliquer dans la limite de la forme de groupe ou sur l'une des formes enfants de la forme de groupe
// sélectionnez toutes les autres formes enfants dans ce groupe et permettez-nous de mettre à l'échelle et de déplacer toutes les formes à la fois.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Créez une forme de groupe de 400 pt x 400 pt et placez-la à l'origine des coordonnées de forme flottante du document.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Définissez la taille du plan de coordonnées interne du groupe sur 500 x 500 pt.
// Le coin supérieur gauche du groupe aura une coordonnée x et y de (0, 0),
// et le coin inférieur droit aura une coordonnée x et y de (500, 500).
group.CoordSize = new Size(500, 500);

 // Définissez les coordonnées du coin supérieur gauche du groupe sur (-250, -250).
// Le centre du groupe aura désormais une valeur de coordonnées x et y de (0, 0),
// et le coin inférieur droit sera à (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Créez un rectangle qui affichera la limite de cette forme de groupe et ajoutez-le au groupe.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Une fois qu'une forme fait partie d'une forme de groupe, nous pouvons y accéder en tant que nœud enfant, puis la modifier.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Créez une petite étoile rouge et insérez-la dans le groupe.
// Alignez la forme avec l'origine des coordonnées du groupe, que nous avons déplacée vers le centre.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Insérez un rectangle, puis insérez un rectangle légèrement plus petit au même endroit avec une image.
// Les nouvelles formes ajoutées au groupe chevauchent les anciennes. Le rectangle bleu clair chevauche partiellement l'étoile rouge.
// et ensuite la forme avec l'image chevauchera le rectangle bleu clair, l'utilisant comme cadre.
// Nous ne pouvons pas utiliser les propriétés « ZOrder » des formes pour manipuler leur disposition au sein d'une forme de groupe.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Insérer une zone de texte dans la forme de groupe. Définissez la propriété « Gauche » pour que le bord droit de la zone de texte soit
// touche la limite droite de la forme du groupe. Définissez la propriété « Haut » pour que la zone de texte se trouve à l'extérieur.
// la limite de la forme du groupe, avec sa taille supérieure alignée le long de la marge inférieure de la forme du groupe.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
