---
title: GradientStop.Position
second_title: Справочник по API Aspose.Words для .NET
description: GradientStop свойство. Получает или задает значение представляющее положение остановки в градиенте  выраженное в процентах в диапазоне от 00 до 10. .
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/gradientstop/position/
---
## GradientStop.Position property

Получает или задает значение, представляющее положение остановки в градиенте , выраженное в процентах в диапазоне от 0,0 до 1,0. .

```csharp
public double Position { get; set; }
```

### Примеры

Показывает, как добавить остановки градиента к градиентной заливке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Получаем коллекцию остановок градиента.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Изменить первую остановку градиента.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Добавляем новую остановку градиента в конец коллекции.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Удалить остановку градиента по индексу 1.
gradientStops.RemoveAt(1);
// И вставляем новую точку градиента с тем же индексом 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Удалить последнюю остановку градиента в коллекции.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Используйте опцию соответствия, чтобы определить форму с помощью DML
// если вы хотите получить свойство «GradientStops» после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Смотрите также

* class [GradientStop](../)
* пространство имен [Aspose.Words.Drawing](../../gradientstop/)
* сборка [Aspose.Words](../../../)


