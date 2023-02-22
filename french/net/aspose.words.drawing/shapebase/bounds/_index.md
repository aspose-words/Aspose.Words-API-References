---
title: ShapeBase.Bounds
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient ou définit lemplacement et la taille du bloc conteneur de la forme.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Obtient ou définit l'emplacement et la taille du bloc conteneur de la forme.

```csharp
public RectangleF Bounds { get; set; }
```

### Remarques

Ignore le verrouillage des proportions lors du réglage.

Pour une forme de niveau supérieur, la valeur est exprimée en points et relative à l'ancre de la forme.

Pour les formes d'un groupe, la valeur est dans l'espace de coordonnées et les unités du groupe parent.

### Exemples

Montre comment vérifier une forme contenant des limites de bloc.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Même si la ligne elle-même prend peu de place sur la page du document,
// il occupe un bloc contenant rectangulaire, dont nous pouvons déterminer la taille à l'aide des propriétés "Bounds".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Crée une forme de groupe, puis définit la taille de son bloc contenant à l'aide de la propriété "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Crée un rectangle, vérifie la taille de son bloc de délimitation, puis ajoute-le à la forme du groupe.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Le plan de coordonnées de la forme du groupe a son origine dans le coin supérieur gauche de son bloc contenant,
// et les coordonnées x et y de (1000, 1000) dans le coin inférieur droit.
// Notre forme de groupe a une taille de 250 x 250 pts, donc tous les 4 pts sur le plan de coordonnées de la forme de groupe
// traduit en 1pt dans le plan de coordonnées du corps du document.
// Chaque forme que nous insérons sera également réduite en taille d'un facteur de 4.
// La modification de la propriété "BoundsInPoints" de la forme reflétera cela.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Insère une forme et la place en dehors des limites du bloc contenant la forme de groupe.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// L'encombrement de la forme de groupe dans le corps du document a augmenté, mais le bloc contenant reste le même.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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


