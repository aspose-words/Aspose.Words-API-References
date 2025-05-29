---
title: ReflectionFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words для .NET
description: Отрегулируйте прозрачность ReflectionFormat от 0,0 (непрозрачный) до 1,0 (прозрачный) для настраиваемых эффектов отражения. Улучшите свои проекты с точностью!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/reflectionformat/transparency/
---
## ReflectionFormat.Transparency property

Возвращает или задает двойное значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности для эффекта отражения. Значение по умолчанию — 0.0.

```csharp
public double Transparency { get; set; }
```

## Примеры

Показывает, как взаимодействовать с эффектом формы отражения.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Смотрите также

* class [ReflectionFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
