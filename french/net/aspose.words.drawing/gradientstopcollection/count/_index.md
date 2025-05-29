---
title: GradientStopCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété GradientStopCollection Count, qui fournit le nombre total d'éléments, améliorant ainsi votre gestion des données et l'efficacité de la conception de l'interface utilisateur.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/gradientstopcollection/count/
---
## GradientStopCollection.Count property

Obtient une valeur entière indiquant le nombre d'éléments dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Montre comment ajouter des arrêts de dégradé au remplissage dégradé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Obtenir la collection d'arrêts de dégradé.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Changer le premier arrêt du dégradé.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Ajouter un nouvel arrêt de dégradé à la fin de la collection.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Supprimer l'arrêt du dégradé à l'index 1.
gradientStops.RemoveAt(1);
// Et insérez un nouvel arrêt de dégradé au même index 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Supprime le dernier arrêt de dégradé de la collection.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML
// si vous souhaitez obtenir la propriété « GradientStops » après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Voir également

* class [GradientStopCollection](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
