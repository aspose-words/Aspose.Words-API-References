---
title: Class ChartTitle
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartTitle сорт. Предоставляет доступ к свойствам заголовка диаграммы.
type: docs
weight: 750
url: /ru/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Предоставляет доступ к свойствам заголовка диаграммы.

```csharp
public class ChartTitle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение равно false. |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Определяет, будет ли отображаться заголовок для этой диаграммы. Значение по умолчанию — true. |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Получает или задает текст заголовка диаграммы. Если указано нулевое или пустое значение, будет показан автоматически сгенерированный заголовок. |

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


