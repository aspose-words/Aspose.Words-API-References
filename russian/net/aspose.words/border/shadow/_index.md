---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words для .NET
description: Border Shadow свойство. Получает или задает значение указывающее имеет ли граница тень на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/border/shadow/
---
## Border.Shadow property

Получает или задает значение, указывающее, имеет ли граница тень.

```csharp
public bool Shadow { get; set; }
```

## Примечания

В Microsoft Word, чтобы граница имела тень, границы на всех четырех сторонах (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и все они должны иметь свойство Тень, установленное в значение`истинный`.

## Примеры

Показывает, как создать зеленую волнистую рамку страницы с тенью.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Смотрите также

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
