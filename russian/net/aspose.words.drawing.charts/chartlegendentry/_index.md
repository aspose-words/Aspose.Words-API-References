---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ChartLegendEntry для создания динамических легенд диаграмм. Улучшите визуализацию данных с помощью бесшовной интеграции и настройки.
type: docs
weight: 1020
url: /ru/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Представляет запись легенды диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartLegendEntry
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Предоставляет доступ к форматированию шрифта этой записи легенды. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Возвращает или задает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию:**ЛОЖЬ** . |

## Примечания

Запись легенды соответствует определенной серии диаграмм или линии тренда.

Текст записи — название серии или линии тренда. Текст не может быть изменен.

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
