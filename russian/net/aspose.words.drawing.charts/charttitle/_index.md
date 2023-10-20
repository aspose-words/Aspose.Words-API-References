---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartTitle сорт. Предоставляет доступ к свойствам заголовка диаграммы на С#.
type: docs
weight: 820
url: /ru/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Предоставляет доступ к свойствам заголовка диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами ](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartTitle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение установлено.`ЛОЖЬ` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Определяет, будет ли отображаться заголовок для этой диаграммы. Значение по умолчанию:`истинный` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Получает или задает текст заголовка диаграммы. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок. |

## Примеры

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
