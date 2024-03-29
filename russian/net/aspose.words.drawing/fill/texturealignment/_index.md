---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words для .NET
description: Fill TextureAlignment свойство. Получает или задает выравнивание для заливки текстуры плитки на С#.
type: docs
weight: 180
url: /ru/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Получает или задает выравнивание для заливки текстуры плитки.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
