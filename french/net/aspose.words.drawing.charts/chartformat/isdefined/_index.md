---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words pour .NET
description: Découvrez si un format est défini avec la propriété ChartFormat IsDefined. Bénéficiez dès aujourd'hui d'un contrôle de mise en forme transparent pour vos graphiques !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Obtient un indicateur indiquant si un format est défini.

```csharp
public bool IsDefined { get; }
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
