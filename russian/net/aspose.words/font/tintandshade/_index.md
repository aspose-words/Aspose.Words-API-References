---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font TintAndShade для легкой настройки цветов! Осветляйте или затемняйте оттенки для ярких дизайнов. Улучшайте свои проекты без усилий!
type: docs
weight: 530
url: /ru/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет.

```csharp
public double TintAndShade { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызвать исключение, если установить это свойство равным значению меньше -1 или больше 1. |
| InvalidOperationException | Вызвать, если задать это свойство для[`Font`](../) объект с нетематическими цветами. |

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый).

Ноль (0) нейтрален.

## Примеры

Показывает, как создавать и использовать тематический стиль.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Создайте стиль с использованием свойств шрифта темы.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
