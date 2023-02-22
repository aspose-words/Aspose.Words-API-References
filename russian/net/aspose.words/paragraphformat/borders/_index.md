---
title: ParagraphFormat.Borders
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает набор границ абзаца.
type: docs
weight: 50
url: /ru/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Получает набор границ абзаца.

```csharp
public BorderCollection Borders { get; }
```

### Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


