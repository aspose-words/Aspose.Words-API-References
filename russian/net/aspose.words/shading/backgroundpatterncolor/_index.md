---
title: Shading.BackgroundPatternColor
second_title: Справочник по API Aspose.Words для .NET
description: Shading свойство. Получает или задает цвет применяемый к фонуShading объект.
type: docs
weight: 10
url: /ru/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Получает или задает цвет, применяемый к фону[`Shading`](../) объект.

```csharp
public Color BackgroundPatternColor { get; set; }
```

### Примеры

Показывает, как украшать текст границами и заливкой.

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
* пространство имен [Aspose.Words](../../shading/)
* сборка [Aspose.Words](../../../)


