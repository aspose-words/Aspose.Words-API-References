---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartDataPoint Explosion pour ajuster les points de données des graphiques à secteurs. Contrôlez le mouvement depuis le centre pour des visualisations percutantes. Améliorez vos graphiques dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

Spécifie la quantité de déplacement du point de données par rapport au centre du graphique à secteurs. Peut être négatif, ce qui signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques à secteurs.

```csharp
public int Explosion { get; set; }
```

## Exemples

Montre comment déplacer les tranches d'un graphique à secteurs loin du centre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Les « tranches » d'un graphique à secteurs peuvent être éloignées du centre d'une certaine distance via l'attribut Explosion du point de données respectif.
// Ajoutez un point de données à la première partie du graphique à secteurs et éloignez-le du centre de 10 points.
// Aspose.Words crée automatiquement des points de données s'ils n'existent pas.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Déplacez la deuxième partie d'une plus grande distance.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Voir également

* class [ChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
