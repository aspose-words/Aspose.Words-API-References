---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Shape FillColor, чтобы персонализировать свои проекты с помощью ярких цветов кисти, которые улучшат ваши формы и выведут ваши проекты на новый уровень.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Определяет цвет кисти, заполняющей замкнутый контур фигуры.

```csharp
public Color FillColor { get; set; }
```

## Примечания

Это ярлык для[`Color`](../../fill/color/) свойство.

Значение по умолчанию: White .

## Примеры

Показывает, как залить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите текст, а затем закройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство "StrokeColor", чтобы задать цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство «FillColor», чтобы задать цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство «Непрозрачность» определяет прозрачность цвета по шкале от 0 до 1,
// где 1 — полностью непрозрачный, а 0 — невидимый.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, над которым находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите меньшее значение непрозрачности цвета заливки фигуры, чтобы мы могли видеть текст под ней.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
