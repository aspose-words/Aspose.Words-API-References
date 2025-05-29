---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.TextureAlignment для точного выравнивания заливки текстур. Улучшите дизайн документов с помощью бесшовных вариантов плитки!
type: docs
weight: 1780
url: /ru/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Задает выравнивание для мозаичного размещения текстурной заливки.

```csharp
public enum TextureAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| TopLeft | `0` | Верхнее левое выравнивание текстуры. |
| Top | `1` | Верхнее выравнивание текстуры. |
| TopRight | `2` | Верхнее правое выравнивание текстуры. |
| Left | `3` | Выравнивание текстуры по левому краю. |
| Center | `4` | Выравнивание текстуры по центру. |
| Right | `5` | Правое выравнивание текстуры. |
| BottomLeft | `6` | Нижнее левое выравнивание текстуры. |
| Bottom | `7` | Выравнивание нижней текстуры. |
| BottomRight | `8` | Нижнее правое выравнивание текстуры. |
| None | `9` | Нет выравнивания текстуры. |

## Примеры

Показывает, как заполнять и размещать текстуру внутри фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Применить выравнивание текстуры к заливке фигуры.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Используйте параметр соответствия, чтобы определить форму с помощью DML, если вы хотите получить "TextureAlignment"
// свойство после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
