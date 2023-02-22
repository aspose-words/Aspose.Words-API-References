---
title: Fill.TextureAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Fill свойство. Получает или задает выравнивание для заливки текстурой тайла.
type: docs
weight: 130
url: /ru/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Получает или задает выравнивание для заливки текстурой тайла.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../fill/)
* сборка [Aspose.Words](../../../)


