---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GlowFormat Color, чтобы настроить эффекты свечения. Легко устанавливайте яркие цвета для потрясающего визуального эффекта. По умолчанию — черный.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Получает или задаетColor объект, представляющий цвет для эффекта свечения. Значение по умолчанию:Black .

```csharp
public Color Color { get; set; }
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

* class [GlowFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
