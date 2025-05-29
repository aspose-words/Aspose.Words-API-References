---
title: Shading.ForegroundPatternColor
linktitle: ForegroundPatternColor
articleTitle: ForegroundPatternColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Shading ForegroundPatternColor, чтобы настроить цвет переднего плана объекта Shading для улучшения дизайна и визуальной привлекательности.
type: docs
weight: 40
url: /ru/net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

Возвращает или задает цвет, применяемый к переднему плану[`Shading`](../) объект.

```csharp
public Color ForegroundPatternColor { get; set; }
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
