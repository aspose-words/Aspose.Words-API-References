---
title: IChartDataPoint.Explosion
second_title: Справочник по API Aspose.Words для .NET
description: IChartDataPoint свойство. Определяет величину на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным отрицательное значение означает что свойство не установлено и разнесение не должно применяться. Применяется только к круговым диаграммам.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным, отрицательное значение означает, что свойство не установлено и разнесение не должно применяться. Применяется только к круговым диаграммам.

```csharp
public int Explosion { get; set; }
```

### Примеры

Показывает, как переместить фрагменты круговой диаграммы от центра.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// «Срезы» круговой диаграммы можно отодвинуть от центра на некоторое расстояние с помощью атрибута Explosion соответствующей точки данных.
// Добавьте точку данных в первую часть круговой диаграммы и переместите ее от центра на 10 точек.
// Aspose.Words автоматически создает точки данных, если их не существует.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Сместим вторую часть на большее расстояние.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Смотрите также

* interface [IChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* сборка [Aspose.Words](../../../)


