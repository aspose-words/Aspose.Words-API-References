---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.GradientStopCollection classe. Contient une collection deGradientStop objets en C#.
type: docs
weight: 990
url: /fr/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

Contient une collection de[`GradientStop`](../gradientstop/) objets.

Pour en savoir plus, visitez le[Travailler avec des éléments graphiques](https://docs.aspose.com/words/net/working-with-graphic-elements/) article documentaire.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | Obtient une valeur entière indiquant le nombre d'éléments dans la collection. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | Obtient ou définit un[`GradientStop`](../gradientstop/) objet dans la collection. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | Ajoute un spécifié[`GradientStop`](../gradientstop/) à un dégradé. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | Renvoie un énumérateur qui parcourt la collection. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | Insère un[`GradientStop`](../gradientstop/) à la collection à un index spécifié. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | Supprime un spécifié[`GradientStop`](../gradientstop/) de la collection. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | Supprime un[`GradientStop`](../gradientstop/) de la collection à un index spécifié. |

## Remarques

Vous ne créez pas directement d'instances de cette classe. Utilisez le[`GradientStops`](../fill/gradientstops/)propriété pour accéder aux arrêts de dégradé des objets de remplissage.

## Exemples

Montre comment ajouter des points de dégradé au remplissage dégradé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Récupère la collection d'arrêts de dégradé.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Change le premier arrêt du dégradé.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Ajoute un nouveau point de dégradé à la fin de la collection.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Supprime l'arrêt du dégradé à l'index 1.
gradientStops.RemoveAt(1);
// Et insérez un nouveau point de dégradé au même index 1.
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
// si vous souhaitez obtenir la propriété "GradientStops" après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Voir également

* class [GradientStop](../gradientstop/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
