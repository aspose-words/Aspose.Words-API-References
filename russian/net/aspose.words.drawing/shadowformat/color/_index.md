---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShadowFormat Color, чтобы настроить цвета теней в ваших проектах. По умолчанию — черный, но дайте волю своему творчеству с яркими вариантами!
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

ПолучаетColor объект, представляющий цвет тени. Значение по умолчанию:Black .

```csharp
public Color Color { get; }
```

## Примеры

Показывает, как получить цвет тени.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Смотрите также

* class [ShadowFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
