---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words для .NET
description: Откройте для себя свойство прозрачности GlowFormat, легко настройте эффекты свечения от непрозрачного до прозрачного (от 0,0 до 1,0) для потрясающего визуального эффекта. По умолчанию 0,0.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Возвращает или задает степень прозрачности для эффекта свечения в виде значения от 0,0 (непрозрачный) до 1,0 (прозрачный). Значение по умолчанию — 0,0.

```csharp
public double Transparency { get; set; }
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
