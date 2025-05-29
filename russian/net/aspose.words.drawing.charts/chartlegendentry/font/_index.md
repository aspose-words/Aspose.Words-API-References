---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Откройте для себя свойство шрифта ChartLegendEntry для легкого доступа к настраиваемому форматированию шрифта, улучшающему визуальное оформление записей легенд.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Предоставляет доступ к форматированию шрифта этой записи легенды.

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
* class [ChartLegendEntry](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
