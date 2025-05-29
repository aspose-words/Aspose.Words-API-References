---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GlowFormat Radius для настройки эффектов свечения. Отрегулируйте радиус в точках для потрясающих визуальных улучшений. По умолчанию 0,0.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

Возвращает или задает двойное значение, представляющее длину радиуса для эффекта свечения в пунктах (pt). Значение по умолчанию — 0.0.

```csharp
public double Radius { get; set; }
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
