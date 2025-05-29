---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: Aspose.Words для .NET
description: Улучшите свои проекты с помощью ShapeBase Glow! Добейтесь потрясающих эффектов свечения для своих фигур и улучшите свои визуальные проекты без особых усилий.
type: docs
weight: 200
url: /ru/net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Получает форматирование свечения для фигуры.

```csharp
public GlowFormat Glow { get; }
```

## Примеры

Показывает, как взаимодействовать с эффектом свечения.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Смотрите также

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
