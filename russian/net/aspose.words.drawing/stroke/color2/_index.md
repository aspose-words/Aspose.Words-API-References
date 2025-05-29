---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Stroke Color2 — улучшите свои проекты с помощью настраиваемого второго цвета обводки для создания ярких, привлекающих внимание визуальных эффектов.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Определяет второй цвет для обводки.

```csharp
public Color Color2 { get; set; }
```

## Примечания

Значение по умолчанию для[`Shape`](../../shape/) is White .

## Примеры

Показывает, как обрабатывать элементы обводки формы.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Обводки могут иметь два цвета, которые используются для создания узора, определяемого двухцветными данными изображения.
// Обводки одного цвета не используют свойство Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Смотрите также

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
