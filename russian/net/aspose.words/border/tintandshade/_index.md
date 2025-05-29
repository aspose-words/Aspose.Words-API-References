---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words для .NET
description: Откройте для себя Border TintAndShade, легко настройте яркость цвета с помощью простого двойного значения для потрясающих улучшений дизайна. Идеально подходит для ваших творческих проектов!
type: docs
weight: 80
url: /ru/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет.

```csharp
public double TintAndShade { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывает исключение при попытке установить это свойство на значение меньше -1 или больше 1. |
| InvalidOperationException | Вызывает ошибку, если это свойство задано для объекта Border с цветами, не соответствующими теме. |

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным.

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

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
