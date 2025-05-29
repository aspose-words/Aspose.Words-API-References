---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство ImageBytes для создания потрясающих изображений штрихов и уникальных узорных заливок для ваших дизайнов. Улучшите свои визуальные эффекты сегодня!
type: docs
weight: 160
url: /ru/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Определяет изображение для штрихового изображения или узорной заливки.

```csharp
public byte[] ImageBytes { get; }
```

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
