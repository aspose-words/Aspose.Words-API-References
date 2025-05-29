---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words для .NET
description: Настройте свойство ForeTintAndShade, чтобы легко осветлить или затемнить цвет переднего плана, придав дизайну точность и креативность.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет переднего плана.

```csharp
public double ForeTintAndShade { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызвать исключение, если установить это свойство равным значению меньше -1 или больше 1. |

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый).

Ноль (0) нейтрален.

## Примеры

Показывает, как управлять осветлением и затемнением цвета шрифта переднего плана.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
