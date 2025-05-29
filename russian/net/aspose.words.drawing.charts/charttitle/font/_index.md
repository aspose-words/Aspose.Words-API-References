---
title: ChartTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Настройте заголовок диаграммы с помощью свойства ChartTitle Font для улучшенного форматирования шрифта. Улучшите представление данных без усилий!
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/charttitle/font/
---
## ChartTitle.Font property

Предоставляет доступ к форматированию шрифта заголовка диаграммы.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartTitle](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
