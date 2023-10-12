---
title: Class Chart
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.Chart сорт. Обеспечивает доступ к свойствам фигуры диаграммы.
type: docs
weight: 620
url: /ru/net/aspose.words.drawing.charts/chart/
---
## Chart class

Обеспечивает доступ к свойствам фигуры диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class Chart
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Получает коллекцию всех осей этой диаграммы. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Обеспечивает доступ к свойствам оси X диаграммы. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Обеспечивает доступ к свойствам оси Y диаграммы. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Обеспечивает доступ к свойствам оси Z диаграммы. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Обеспечивает доступ к свойствам легенды диаграммы. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Предоставляет доступ к коллекции серий. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Получает путь и имя файла xls/xlsx, с которым связана эта диаграмма. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Предоставляет доступ к свойствам заголовка диаграммы. |

### Примеры

Показывает, как вставить диаграмму и задать заголовок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте фигуру диаграммы с помощью конструктора документов и получите ее диаграмму.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Используйте свойство «Title», чтобы присвоить нашей диаграмме заголовок, который появится в верхней центральной части области диаграммы.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Установите для свойства «Показать» значение «истина», чтобы сделать заголовок видимым.
title.Show = true;

// Установите для свойства Overlay значение true. Дайте другим элементам диаграммы больше места, разрешив им перекрывать заголовок.
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


