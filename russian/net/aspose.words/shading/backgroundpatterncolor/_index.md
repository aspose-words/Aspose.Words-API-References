---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Shading BackgroundPatternColor, чтобы настроить цвет фона объекта Shading и улучшить визуальную привлекательность вашего дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Возвращает или задает цвет, применяемый к фону[`Shading`](../) объект.

```csharp
public Color BackgroundPatternColor { get; set; }
```

## Примеры

Показывает, как оформить текст с помощью границ и заливки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Смотрите также

* class [Shading](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
