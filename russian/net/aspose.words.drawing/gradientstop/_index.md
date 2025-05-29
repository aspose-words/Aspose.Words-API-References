---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.GradientStop — решение для создания потрясающих градиентов с настраиваемыми остановками для улучшения визуального восприятия документов.
type: docs
weight: 1310
url: /ru/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Представляет одну остановку градиента.

Чтобы узнать больше, посетите[Работа с графическими элементами](https://docs.aspose.com/words/net/working-with-graphic-elements/) документальная статья.

```csharp
public class GradientStop
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Инициализирует новый экземпляр`GradientStop` класс. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Инициализирует новый экземпляр`GradientStop` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Получает значение, представляющее цвет остановки градиента без каких-либо модификаторов. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Возвращает или задает значение, представляющее цвет остановки градиента. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Возвращает или задает значение, представляющее положение остановки в пределах градиента , выраженное в процентах в диапазоне от 0,0 до 1,0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Возвращает или задает значение, представляющее прозрачность градиентной заливки , выраженное в процентах в диапазоне от 0,0 до 1,0. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Удаляет точку остановки градиента из родительского объекта[`GradientStopCollection`](../gradientstopcollection/) . |

## Примеры

Показывает, как добавлять точки градиента к градиентной заливке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Получить коллекцию остановок градиента.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Изменить первую точку остановки градиента.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Добавляем новую точку остановки градиента в конец коллекции.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Удалить остановку градиента по индексу 1.
gradientStops.RemoveAt(1);
// И вставляем новую точку остановки градиента с тем же индексом 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Удалить последнюю точку градиента в коллекции.
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

// Используйте параметр соответствия для определения формы с помощью DML
// если вы хотите получить свойство "GradientStops" после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
