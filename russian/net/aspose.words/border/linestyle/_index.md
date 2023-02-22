---
title: Border.LineStyle
second_title: Справочник по API Aspose.Words для .NET
description: Border свойство. Получает или задает стиль границы.
type: docs
weight: 40
url: /ru/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Получает или задает стиль границы.

```csharp
public LineStyle LineStyle { get; set; }
```

### Примечания

Если вы установите для стиля линии значение none, то ширина линии автоматически изменится на ноль.

### Примеры

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* пространство имен [Aspose.Words](../../border/)
* сборка [Aspose.Words](../../../)


