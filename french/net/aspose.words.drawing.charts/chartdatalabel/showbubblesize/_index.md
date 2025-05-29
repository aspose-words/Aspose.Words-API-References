---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ShowBubbleSize améliore vos graphiques à bulles en affichant la taille des étiquettes de données. Optimisez la représentation visuelle de vos données dès aujourd'hui !
type: docs
weight: 130
url: /fr/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données sur un graphique. S'applique uniquement aux graphiques à bulles. La valeur par défaut est`FAUX` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## Exemples

Montre comment utiliser les effets 3D avec les graphiques à bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Appliquez une étiquette de données à chaque bulle qui affiche son diamètre.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Voir également

* class [ChartDataLabel](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
