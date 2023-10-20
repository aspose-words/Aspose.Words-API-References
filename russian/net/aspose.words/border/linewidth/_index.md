---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words для .NET
description: Border LineWidth свойство. Получает или задает ширину границы в пунктах на С#.
type: docs
weight: 50
url: /ru/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Получает или задает ширину границы в пунктах.

```csharp
public double LineWidth { get; set; }
```

## Примечания

Если вы установите ширину линии больше нуля, когда стиль линии равен «Нет», стиль линии is автоматически изменится на одинарную.

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
