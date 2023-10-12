---
title: Class ChartAxisCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartAxisCollection klass. Representerar en samling av diagramaxlar.
type: docs
weight: 640
url: /sv/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Representerar en samling av diagramaxlar.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Hämtar antalet axlar i den här samlingen. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Hämtar axeln vid angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Returnerar ett uppräkningsobjekt. |

### Exempel

Visar hur man arbetar med yxsamling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Göm de stora rutnätslinjerna på den primära och sekundära Y-axeln.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Se även

* class [ChartAxis](../chartaxis/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


