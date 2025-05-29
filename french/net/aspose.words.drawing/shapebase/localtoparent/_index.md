---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words pour .NET
description: Transformez les coordonnées locales en espace de forme parent avec la méthode ShapeBase LocalToParent. Améliorez la précision de vos projets de modélisation 3D dès aujourd'hui !
type: docs
weight: 680
url: /fr/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Convertit une valeur de l'espace de coordonnées local dans l'espace de coordonnées de la forme parent.

```csharp
public PointF LocalToParent(PointF value)
```

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

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
