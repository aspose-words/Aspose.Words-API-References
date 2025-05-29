---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat Shading для улучшенной стилизации текста. Получите доступ к объекту Shading, чтобы без усилий повысить визуальную привлекательность вашего абзаца.
type: docs
weight: 290
url: /ru/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Возвращает[`Shading`](../../shading/) объект, который ссылается на форматирование штриховки для абзаца.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
