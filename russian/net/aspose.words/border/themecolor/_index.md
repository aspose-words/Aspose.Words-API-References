---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство Border ThemeColor для настройки цветовой схемы и улучшения дизайна с помощью ярких, индивидуально подобранных тем.
type: docs
weight: 70
url: /ru/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Возвращает или задает цвет темы в примененной цветовой схеме, связанной с этим объектом Border.

```csharp
public ThemeColor ThemeColor { get; set; }
```

## Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Устанавливайте ThemeColor только при установке LineWidth или LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
