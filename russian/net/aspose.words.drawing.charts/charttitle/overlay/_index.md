---
title: ChartTitle.Overlay
second_title: Справочник по API Aspose.Words для .NET
description: ChartTitle свойство. Определяет разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение установлено.ЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение установлено.`ЛОЖЬ` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartTitle](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../charttitle/)
* сборка [Aspose.Words](../../../)


