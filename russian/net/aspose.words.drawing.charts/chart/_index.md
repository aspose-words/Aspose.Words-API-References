---
title: Class Chart
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.Chart сорт. Предоставляет доступ к свойствам формы диаграммы.
type: docs
weight: 600
url: /ru/net/aspose.words.drawing.charts/chart/
---
## Chart class

Предоставляет доступ к свойствам формы диаграммы.

```csharp
public class Chart
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Предоставляет доступ к свойствам оси X диаграммы. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Предоставляет доступ к свойствам оси Y диаграммы. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Предоставляет доступ к свойствам оси Z диаграммы. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Предоставляет доступ к свойствам легенды диаграммы. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Предоставляет доступ к коллекции серий. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Получает путь и имя файла xls/xlsx, с которым связана эта диаграмма. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Предоставляет доступ к свойствам заголовка диаграммы. |

### Примеры

Показывает, как вставить диаграмму и установить заголовок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте форму диаграммы с помощью конструктора документов и получите ее диаграмму.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Используйте свойство «Заголовок», чтобы дать нашей диаграмме заголовок, который появляется в верхней центральной части области диаграммы.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Установите для свойства "Show" значение "true", чтобы сделать заголовок видимым.
title.Show = true;

// Установите для свойства "Overlay" значение "true" Дайте другим элементам диаграммы больше места, позволив им перекрывать заголовок
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


