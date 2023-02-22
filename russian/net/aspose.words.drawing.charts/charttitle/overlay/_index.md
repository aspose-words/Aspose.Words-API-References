---
title: ChartTitle.Overlay
second_title: Справочник по API Aspose.Words для .NET
description: ChartTitle свойство. Определяет разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение равно false.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение равно false.

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartTitle](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../charttitle/)
* сборка [Aspose.Words](../../../)


