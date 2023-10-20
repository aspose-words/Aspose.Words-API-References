---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.TextureAlignment перечисление. Определяет выравнивание мозаики заливки текстуры на С#.
type: docs
weight: 1370
url: /ru/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Определяет выравнивание мозаики заливки текстуры.

```csharp
public enum TextureAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| TopLeft | `0` | Выравнивание текстуры вверху слева. |
| Top | `1` | Выравнивание текстуры сверху. |
| TopRight | `2` | Выравнивание текстуры вверху справа. |
| Left | `3` | Выравнивание текстуры по левому краю. |
| Center | `4` | Выравнивание текстуры по центру. |
| Right | `5` | Выравнивание текстуры справа. |
| BottomLeft | `6` | Выравнивание текстуры слева внизу. |
| Bottom | `7` | Выравнивание нижней текстуры. |
| BottomRight | `8` | Выравнивание текстуры справа внизу. |
| None | `9` | Нет выравнивания текстур. |

## Примеры

Показывает, как заполнить и расположить текстуру внутри фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Применяем выравнивание текстуры к заливке фигуры.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Используйте опцию соответствия, чтобы определить форму с помощью DML, если вы хотите получить «TextureAlignment»
// свойство после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
