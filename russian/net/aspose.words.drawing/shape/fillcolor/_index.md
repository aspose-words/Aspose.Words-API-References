---
title: Shape.FillColor
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Определяет цвет кисти заполняющей замкнутый контур фигуры.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Определяет цвет кисти, заполняющей замкнутый контур фигуры.

```csharp
public Color FillColor { get; set; }
```

### Примечания

Это ярлык для[`Color`](../../fill/color/) свойство.

Значение по умолчанию: .White.

### Примеры

Показывает, как залить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите текст, а затем покройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство StrokeColor, чтобы установить цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство FillColor, чтобы установить цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство «Непрозрачность» определяет, насколько прозрачен цвет по шкале от 0 до 1,
// где 1 означает полную непрозрачность, а 0 — невидимость.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, поверх которого находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите меньшее значение непрозрачности цвета заливки фигуры, чтобы мы могли видеть текст под ним.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


