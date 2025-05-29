---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartTitle, который позволит вам легко управлять заголовками диаграмм и настраивать их для улучшенной визуализации данных.
type: docs
weight: 1140
url: /ru/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Предоставляет доступ к свойствам заголовка диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartTitle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Предоставляет доступ к форматированию шрифта заголовка диаграммы. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Предоставляет доступ к заполнению и форматированию строк заголовка диаграммы. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение`ЛОЖЬ` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Определяет, будет ли отображаться заголовок для этой диаграммы. Значение по умолчанию:`истинный` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Получает или задает текст заголовка диаграммы. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок. |

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
