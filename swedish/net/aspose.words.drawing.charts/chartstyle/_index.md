---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words för .NET
description: Använd fördefinierade diagramstilar i Aspose.Words. Förbättra visuella element med ChartStyle-enum för professionell dokumentformatering.
type: docs
weight: 1130
url: /sv/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Anger fördefinierade stilar för ett diagram.

```csharp
public enum ChartStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Representerar standarddiagramformatet. |
| Muted | `1` | En stil med dämpade färger. |
| Saturated | `2` | En stil med mer mättade färger. |
| Shaded | `3` | En stil med skuggade datapunkter. |
| Flat | `4` | En stil med plana datapunkter utan gradient. |
| Shadowed | `5` | En stil med datapunkter som har en skugga. |
| Gradient | `6` | En stil med gradientfyllning av datapunkter. |
| Original | `7` | En stil med ett originellt utseende av ett diagram. |
| Transparent1 | `8` | En stil med transparenta datapunkter. |
| Transparent2 | `9` | En stil med transparenta datapunkter. |
| Outline | `10` | En stil med datapunkter som saknar fyllning, utan endast en disposition. |
| OutlineBlack | `11` | Ett format med svart diagrambakgrund, där datapunkter inte har någon fyllning, utan endast en kontur. |
| Black | `12` | En stil med svart diagrambakgrund. |
| Grey | `13` | En stil med grå tonad diagrambakgrund. |
| Blue | `14` | En stil med blå bakgrund. |
| ShadedPlot | `15` | Ett format där ritningsområdet är skuggat. |

## Exempel

Visar hur man ställer in och hämtar diagramstil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett diagram i svart stil.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Hämta ett diagram att uppdatera.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Hämta diagramstilen.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
