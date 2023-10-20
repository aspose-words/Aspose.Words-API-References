---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: Aspose.Words для .NET
description: Fill Opacity свойство. Получает или задает степень непрозрачности указанной заливки как значение от 00 прозрачный до 10 непрозрачный на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Получает или задает степень непрозрачности указанной заливки как значение от 0,0 (прозрачный) до 1,0 (непрозрачный).

```csharp
public double Opacity { get; set; }
```

## Примечания

Это свойство противоположно свойству[`Transparency`](../transparency/).

## Примеры

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

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
