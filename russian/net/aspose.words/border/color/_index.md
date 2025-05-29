---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Легко настраивайте свои проекты с помощью свойства «Цвет границы», позволяющего вам устанавливать и изменять цвета границ для создания потрясающего визуального эффекта.
type: docs
weight: 10
url: /ru/net/aspose.words/border/color/
---
## Border.Color property

Получает или задает цвет границы.

```csharp
public Color Color { get; set; }
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

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
