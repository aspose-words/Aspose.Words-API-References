---
title: TextureAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Задает выравнивание для мозаичного заполнения текстурной заливкой.
type: docs
weight: 1220
url: /ru/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Задает выравнивание для мозаичного заполнения текстурной заливкой.

```csharp
public enum TextureAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| TopLeft | `0` | Выравнивание текстуры по левому верхнему углу. |
| Top | `1` | Верхнее выравнивание текстуры. |
| TopRight | `2` | Выравнивание текстуры вверху справа. |
| Left | `3` | Выравнивание текстуры по левому краю. |
| Center | `4` | Выравнивание текстуры по центру. |
| Right | `5` | Правильное выравнивание текстуры. |
| BottomLeft | `6` | Выравнивание текстуры по левому нижнему краю. |
| Bottom | `7` | Выравнивание текстуры по низу. |
| BottomRight | `8` | Выравнивание текстуры по правому нижнему краю. |
| None | `9` | Нет выравнивания текстур. |

### Примеры

Показывает, как заполнять и размещать текстуру внутри фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Применяем выравнивание текстуры к заливке формы.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Используйте параметр соответствия для определения формы с помощью DML, если вы хотите получить "TextureAlignment"
// свойство после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
