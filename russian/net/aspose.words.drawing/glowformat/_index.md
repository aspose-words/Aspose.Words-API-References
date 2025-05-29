---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words для .NET
description: Исследуйте класс Aspose.Words.Drawing.GlowFormat, чтобы улучшить ваши документы с помощью потрясающих эффектов свечения. Поднимите свой дизайн с помощью уникальных опций форматирования!
type: docs
weight: 1300
url: /ru/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Представляет форматирование свечения для объекта.

```csharp
public class GlowFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Получает или задаетColor объект, представляющий цвет для эффекта свечения. Значение по умолчанию:Black . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Возвращает или задает двойное значение, представляющее длину радиуса для эффекта свечения в пунктах (pt). Значение по умолчанию — 0.0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Возвращает или задает степень прозрачности для эффекта свечения в виде значения от 0,0 (непрозрачный) до 1,0 (прозрачный). Значение по умолчанию — 0,0. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Удаляет`GlowFormat` из родительского объекта. |

## Примечания

Используйте[`Glow`](../shapebase/glow/) свойство для доступа к свойствам свечения объекта. Вы не создаете экземпляры`GlowFormat` класс напрямую.

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
