---
title: Fill.Opacity
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill propriété. Obtient ou définit le degré dopacité du remplissage spécifié sous la forme dune valeur comprise entre 00 clair et 10 opaque.
type: docs
weight: 150
url: /fr/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Obtient ou définit le degré d'opacité du remplissage spécifié sous la forme d'une valeur comprise entre 0,0 (clair) et 1,0 (opaque).

```csharp
public double Opacity { get; set; }
```

### Remarques

Cette propriété est le contraire de la propriété[`Transparency`](../transparency/).

### Exemples

Montre comment remplir une forme avec une couleur unie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape.StrokeColor = Color.CadetBlue;

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape.FillColor = Color.LightBlue;

// La propriété "Opacité" détermine le degré de transparence de la couleur sur une échelle de 0 à 1,
// avec 1 étant entièrement opaque et 0 étant invisible.
// Le remplissage de la forme par défaut est entièrement opaque, nous ne pouvons donc pas voir le texte sur lequel se trouve cette forme.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Définit l'opacité de la couleur de remplissage de la forme sur une valeur inférieure afin que nous puissions voir le texte en dessous.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


