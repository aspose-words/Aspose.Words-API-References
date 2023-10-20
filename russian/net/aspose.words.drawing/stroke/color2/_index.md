---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words для .NET
description: Stroke Color2 свойство. Определяет второй цвет обводки на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Определяет второй цвет обводки.

```csharp
public Color Color2 { get; set; }
```

## Примечания

Значение по умолчанию для[`Shape`](../../shape/) is White.

## Примеры

Показывает, как обрабатывать элементы обводки фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Штрихи могут иметь два цвета, которые используются для создания узора, определяемого данными двухцветного изображения.
// Обводки одним цветом не используют свойство Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Смотрите также

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
