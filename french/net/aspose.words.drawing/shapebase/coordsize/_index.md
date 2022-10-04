---
title: CoordSize
second_title: Référence de l'API Aspose.Words pour .NET
description: La largeur et la hauteur de lespace de coordonnées à lintérieur du bloc conteneur de cette forme.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc conteneur de cette forme.

```csharp
public Size CoordSize { get; set; }
```

### Remarques

La valeur par défaut est (1000, 1000).

### Exemples

Montre comment translater l'emplacement des coordonnées x et y sur le plan de coordonnées d'une forme vers un emplacement sur le plan de coordonnées de la forme parent.

```csharp
Document doc = new Document();

// Insère une forme de groupe et la place 100 points en dessous et à droite de
// le point d'origine des coordonnées x et y du document.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Utilisez la méthode "LocalToParent" pour déterminer que (0, 0) sur les coordonnées internes x et y du groupe
// se trouve sur (100, 100) du système de coordonnées de sa forme parent. Le parent de la forme de groupe est le document lui-même.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Par défaut, le plan de coordonnées interne d'une forme a le coin supérieur gauche à (0, 0),
// et le coin inférieur droit à (1000, 1000). En raison de sa taille, notre forme de groupe couvre une zone de 500 pt x 500 pt
// dans le plan du document. Cela signifie qu'un mouvement de 1 pt sur le plan de coordonnées du document se traduira
// à un mouvement de 2 points sur le plan de coordonnées de la forme du groupe.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Déplace l'origine des axes x et y de la forme de groupe du coin supérieur gauche vers le centre.
// Cela décalera encore plus les coordonnées internes du groupe par rapport aux coordonnées du document.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// La modification de l'échelle du plan de coordonnées affectera également les emplacements relatifs.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Si l'on souhaite ajouter une forme à ce groupe en définissant son emplacement en fonction d'un emplacement dans le document,
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

// Crée une forme de groupe. Une forme de groupe peut afficher une collection de nœuds de forme enfant.
// Dans Microsoft Word, cliquer dans les limites de la forme de groupe ou sur l'une des formes enfant de la forme de groupe
// sélectionne toutes les autres formes enfants de ce groupe et nous permet de mettre à l'échelle et de déplacer toutes les formes à la fois.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Crée une forme de groupe de 400 pt x 400 pt et la place à l'origine des coordonnées de la forme flottante du document.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Définit la taille du plan de coordonnées interne du groupe sur 500 x 500 pt.
// Le coin supérieur gauche du groupe aura une coordonnée x et y de (0, 0),
// et le coin inférieur droit aura une coordonnée x et y de (500, 500).
group.CoordSize = new Size(500, 500);

 // Définit les coordonnées du coin supérieur gauche du groupe sur (-250, -250).
// Le centre du groupe aura maintenant une valeur de coordonnées x et y de (0, 0),
// et le coin inférieur droit sera à (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Crée un rectangle qui affichera la limite de cette forme de groupe et l'ajoutera au groupe.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Une fois qu'une forme fait partie d'une forme de groupe, nous pouvons y accéder en tant que nœud enfant, puis la modifier.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Crée une petite étoile rouge et l'insère dans le groupe.
// Alignez la forme avec l'origine des coordonnées du groupe, que nous avons déplacée vers le centre.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

 // Insère un rectangle, puis insère un rectangle légèrement plus petit au même endroit avec une image.
// Les nouvelles formes que nous ajoutons au groupe chevauchent les anciennes formes. Le rectangle bleu clair chevauchera partiellement l'étoile rouge,
// puis la forme avec l'image chevauchera le rectangle bleu clair, en l'utilisant comme cadre.
 // Nous ne pouvons pas utiliser les propriétés "ZOrder" des formes pour manipuler leur disposition dans une forme de groupe.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Insère une zone de texte dans la forme du groupe. Définissez la propriété "Left" de sorte que le bord droit de la zone de texte
// touche la limite droite de la forme du groupe. Définissez la propriété "Top" de sorte que la zone de texte se trouve à l'extérieur
// la limite de la forme de groupe, avec sa taille supérieure alignée le long de la marge inférieure de la forme de groupe.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
