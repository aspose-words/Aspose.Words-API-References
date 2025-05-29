---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Anpassa dina ChartLegend-teckensnittsinställningar utan ansträngning! Få tillgång till standardformatering och åsidosätt enkelt specifika förklaringar för ett elegant utseende.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Ger åtkomst till standardteckensnittsformateringen för förklaringsposter. För att åsidosätta teckensnittsformateringen för en specifik förklaringspost, använd[`Font`](../../chartlegendentry/font/) egendom.

```csharp
public Font Font { get; }
```

## Exempel

Visar hur man arbetar med ett teckensnitt för förklaringar.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Ange standardteckenstorlek för alla förklaringar.
chartLegend.Font.Size = 14;
// Ändra teckensnitt för specifik förklaring.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Hämta förklaringspost för diagramserier.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Se även

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
