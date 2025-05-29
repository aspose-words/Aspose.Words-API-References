---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Border, которое предоставляет настраиваемый объект Border для улучшения стиля шрифта и гибкости дизайна.
type: docs
weight: 60
url: /ru/net/aspose.words/font/border/
---
## Font.Border property

Возвращает[`Border`](../../border/) объект, задающий границу для шрифта.

```csharp
public Border Border { get; }
```

## Примеры

Показывает, как вставить в документ строку, окруженную рамкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
