---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words для .NET
description: Border TintAndShade свойство. Получает или задает двойное значение которое осветляет или затемняет цвет на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Получает или задает двойное значение, которое осветляет или затемняет цвет.

```csharp
public double TintAndShade { get; set; }
```

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

Установка этого свойства для объекта Border с цветовой гаммой, не относящейся к теме, приводит кInvalidOperationException.

## Примеры

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

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
