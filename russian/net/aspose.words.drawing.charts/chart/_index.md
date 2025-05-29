---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words для .NET
description: Разблокируйте мощные свойства формы диаграммы с классом Aspose.Words.Drawing.Charts.Chart. Улучшите свои документы с помощью динамического визуального представления данных.
type: docs
weight: 880
url: /ru/net/aspose.words.drawing.charts/chart/
---
## Chart class

Предоставляет доступ к свойствам формы диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class Chart
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Получает коллекцию всех осей этой диаграммы. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Предоставляет доступ к свойствам основной оси X диаграммы. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Предоставляет доступ к свойствам основной оси Y диаграммы. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Предоставляет доступ к свойствам оси Z диаграммы. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Предоставляет доступ к свойствам таблицы данных этой диаграммы. Таблицу данных можно отобразить с помощью[`Show`](../chartdatatable/show/) свойство. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Предоставляет доступ к заполнению и форматированию линий диаграммы. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Предоставляет доступ к свойствам легенды диаграммы. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Предоставляет доступ к коллекции серий. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Предоставляет доступ к коллекции групп серий этой диаграммы. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Получает путь и имя файла xls/xlsx, с которым связана эта диаграмма. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Получает или задает стиль диаграммы. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Предоставляет доступ к свойствам заголовка диаграммы. |

## Примеры

Показывает, как вставить диаграмму и задать заголовок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте форму диаграммы с помощью конструктора документов и получите ее диаграмму.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Используйте свойство «Заголовок», чтобы задать заголовок нашей диаграммы, который отображается в верхней центральной части области диаграммы.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Установите свойство «Показать» в значение «true», чтобы сделать заголовок видимым.
title.Show = true;

// Установите свойство «Overlay» на «true» Дайте другим элементам диаграммы больше места, разрешив им перекрывать заголовок
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
