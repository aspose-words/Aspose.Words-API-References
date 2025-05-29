---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words для .NET
description: Установите свойство TextureAlignment для оптимизации заполнения текстуры плитки. Легко настройте выравнивание для улучшения визуальной привлекательности и точности дизайна.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Получает или задает выравнивание для заливки текстуры плитки.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
