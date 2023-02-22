---
title: IChartDataPoint.Explosion
second_title: Référence de l'API Aspose.Words pour .NET
description: IChartDataPoint propriété. Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif négatif signifie que la propriété nest pas définie et quaucune explosion ne doit être appliquée. Sapplique uniquement aux graphiques à secteurs.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques à secteurs.

```csharp
public int Explosion { get; set; }
```

### Exemples

Montre comment éloigner les tranches d'un graphique à secteurs du centre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Les "tranches" d'un graphique à secteurs peuvent être éloignées du centre d'une certaine distance via l'attribut Explosion du point de données respectif.
// Ajoutez un point de données à la première partie du graphique à secteurs et éloignez-le du centre de 10 points.
// Aspose.Words crée automatiquement des points de données s'ils n'existent pas.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Déplace la seconde portion d'une plus grande distance.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Voir également

* interface [IChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* Assemblée [Aspose.Words](../../../)


