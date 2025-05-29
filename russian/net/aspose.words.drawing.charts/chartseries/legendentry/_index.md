---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries LegendEntry, чтобы легко получать доступ к записям легенд для ваших диаграмм и настраивать их, улучшая визуализацию данных.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Получает запись легенды для этой серии диаграмм.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Примеры

Показывает, как работать со шрифтом легенды.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Установить размер шрифта по умолчанию для всех записей легенды.
chartLegend.Font.Size = 14;
// Изменить шрифт для определенной записи легенды.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Получить запись легенды для серии диаграмм.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Смотрите также

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
