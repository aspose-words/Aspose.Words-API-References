---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la méthode ChartFormat SetDefaultFill pour restaurer sans effort le remplissage de votre élément de graphique à sa valeur par défaut d'origine.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Réinitialise le remplissage de l'élément de graphique pour avoir la valeur par défaut.

```csharp
public void SetDefaultFill()
```

## Exemples

Montre comment réinitialiser le remplissage à la valeur par défaut définie dans la série.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Voir également

* class [ChartFormat](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
