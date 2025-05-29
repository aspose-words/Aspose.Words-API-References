---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ChartSeries CopyFormatFrom pour répliquer sans effort les formats de points de données par index, améliorant ainsi l'efficacité et la cohérence de vos graphiques.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Copie le format de point de données par défaut à partir du point de données avec l'index spécifié.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Exemples

Montre comment copier le format des points de données.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Obtenez le graphique et la série pour mettre à jour le format.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Copier le format du point de données avec l'index 1 vers le point de données avec l'index 2
// pour que le point de données 2 ressemble au point de données 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Copiez le format du point de données avec l'index 0 vers les valeurs par défaut de la série afin que tous les points de données
// dans la série qui a le format par défaut, ressemble au point de données 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Voir également

* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
