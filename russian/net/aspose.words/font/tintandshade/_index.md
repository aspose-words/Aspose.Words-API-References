---
title: Font.TintAndShade
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает двойное значение которое делает цвет светлее или темнее.
type: docs
weight: 520
url: /ru/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Получает или задает двойное значение, которое делает цвет светлее или темнее.

```csharp
public double TintAndShade { get; set; }
```

### Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

Установка этого свойства для объекта Font с не относящимися к теме colors приводит кInvalidOperationException.

### Примеры

Показывает, как создавать и использовать тематический стиль.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Создадим какой-нибудь стиль со свойствами шрифта темы.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


