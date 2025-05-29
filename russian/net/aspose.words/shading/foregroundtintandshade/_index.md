---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words для .NET
description: Настройте свойство ForegroundTintAndShade, чтобы легко осветлить или затемнить цвета темы, повысив визуальную привлекательность вашего дизайна.
type: docs
weight: 60
url: /ru/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет темы переднего плана.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызвать исключение, если установить это свойство равным значению меньше -1 или больше 1. |
| InvalidOperationException | Вызвать, если это свойство задано для объекта затенения с цветами, не соответствующими теме. |

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый).

Ноль (0) нейтрален.

## Примеры

Показывает, как задать цвета переднего плана и фона для текстуры затенения.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Смотрите также

* class [Shading](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
