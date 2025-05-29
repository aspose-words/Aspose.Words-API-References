---
title: ChartDataPointCollection.CopyFormat
linktitle: CopyFormat
articleTitle: CopyFormat
second_title: Aspose.Words pour .NET
description: Copiez facilement la mise en forme entre les points de données grâce à la méthode ChartDataPointCollection CopyFormat. Améliorez la visualisation de vos données dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection.CopyFormat method

Copie le format du point de données source vers le point de données de destination.

```csharp
public void CopyFormat(int sourceIndex, int destinationIndex)
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

* class [ChartDataPointCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
