---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words для .NET
description: Откройте для себя метод Fill Solid, позволяющий добиться однородной цветовой заливки, без труда повышая визуальную привлекательность и однородность вашего дизайна.
type: docs
weight: 260
url: /ru/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Устанавливает однородный цвет заливки.

```csharp
public void Solid()
```

## Примечания

Используйте этот метод для преобразования любой заливки обратно в сплошную заливку.

## Примеры

Показывает, как преобразовать любую заливку обратно в сплошную.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Получить объект Fill для шрифта первого прогона.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Проверьте свойства заливки шрифта.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Измените тип заливки на Сплошную с равномерным зеленым цветом.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Устанавливает заливку указанным однородным цветом.

```csharp
public void Solid(Color color)
```

## Примечания

Используйте этот метод для преобразования любой заливки обратно в сплошную заливку.

## Примеры

Показывает, как использовать форматирование диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Удалить серию, созданную по умолчанию.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Форматировать фон диаграммы.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Скрыть метки делений осей.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Форматировать заголовок диаграммы.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Форматировать заголовок оси.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Формат легенды.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
