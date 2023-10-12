---
title: ShapeBase.Fill
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает форматирование заливки фигуры.
type: docs
weight: 170
url: /ru/net/aspose.words.drawing/shapebase/fill/
---
## ShapeBase.Fill property

Получает форматирование заливки фигуры.

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../fill/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


