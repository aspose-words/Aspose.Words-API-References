---
title: ParagraphFormat.Shading
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Возвращает объект Shading который ссылается на форматирование затенения абзаца.
type: docs
weight: 270
url: /ru/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Возвращает объект Shading, который ссылается на форматирование затенения абзаца.

```csharp
public Shading Shading { get; }
```

### Примеры

Показывает, как украсить текст рамками и заливкой.

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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


