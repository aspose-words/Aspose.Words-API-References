---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words для .NET
description: Отрегулируйте свойство Border LineWidth, чтобы задать толщину границы в пунктах, повысив точность и визуальную привлекательность вашего дизайна.
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

Если задать толщину линии больше нуля, а стиль линии отсутствует, стиль линии is автоматически изменится на одинарную линию.

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
