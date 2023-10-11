---
title: ParagraphFormat.Borders
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает коллекцию границ абзаца.
type: docs
weight: 60
url: /ru/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Получает коллекцию границ абзаца.

```csharp
public BorderCollection Borders { get; }
```

### Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Устанавливаем ThemeColor только в том случае, если установлены LineWidth или LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


