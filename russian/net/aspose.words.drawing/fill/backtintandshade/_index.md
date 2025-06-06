---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words для .NET
description: Настройте свойство BackTintAndShade, чтобы легко осветлить или затемнить цвет фона, повысив визуальную привлекательность дизайна и удобство использования.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет фона.

```csharp
public double BackTintAndShade { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызвать исключение, если установить это свойство равным значению меньше -1 или больше 1. |

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый).

Ноль (0) нейтрален.

## Примеры

Показывает, как установить цвет темы для цвета фигуры переднего плана/фона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Примечание: не используйте «BackThemeColor» и «BackTintAndShade» для заливки шрифта.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
