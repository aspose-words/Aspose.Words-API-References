---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words для .NET
description: Узнайте, как легко задать свойство PresetTexture и улучшить свои проекты с помощью потрясающих вариантов заливки. Раскройте свой творческий потенциал сегодня!
type: docs
weight: 170
url: /ru/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Получает[`PresetTexture`](../../presettexture/) для заполнения.

```csharp
public PresetTexture PresetTexture { get; }
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
