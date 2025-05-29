---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Настройте параметры шрифта ChartLegend без особых усилий! Получите доступ к форматированию по умолчанию и легко переопределите определенные записи легенды для создания изысканного вида.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Предоставляет доступ к форматированию шрифта по умолчанию для записей легенды. Чтобы переопределить форматирование шрифта для конкретной записи легенды, используйте[`Font`](../../chartlegendentry/font/) свойство.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
