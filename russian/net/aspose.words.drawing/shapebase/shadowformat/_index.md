---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase ShadowFormat, чтобы улучшить свои проекты с помощью настраиваемых эффектов тени для фигур. Повысьте свою визуальную привлекательность сегодня!
type: docs
weight: 520
url: /ru/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Получает форматирование тени для фигуры.

```csharp
public ShadowFormat ShadowFormat { get; }
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

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
