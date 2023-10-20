---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words для .NET
description: Font TintAndShade свойство. Получает или задает двойное значение которое осветляет или затемняет цвет на С#.
type: docs
weight: 520
url: /ru/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Получает или задает двойное значение, которое осветляет или затемняет цвет.

```csharp
public double TintAndShade { get; set; }
```

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

Установка этого свойства для[`Font`](../) объект с цветовой гаммой, не относящейся к теме, приводит кInvalidOperationException.

## Примеры

Показывает, как создавать и использовать тематический стиль.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Создайте стиль с помощью свойств шрифта темы.
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
