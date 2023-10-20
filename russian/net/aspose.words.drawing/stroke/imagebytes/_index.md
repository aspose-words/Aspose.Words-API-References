---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words для .NET
description: Stroke ImageBytes свойство. Определяет изображение для обводки или заливки узором на С#.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Определяет изображение для обводки или заливки узором.

```csharp
public byte[] ImageBytes { get; }
```

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
