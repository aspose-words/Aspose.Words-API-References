---
title: ThemeFont Enum
linktitle: ThemeFont
articleTitle: ThemeFont
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words ThemeFont, чтобы легко управлять шрифтами тем документов и улучшать визуальную привлекательность ваших документов с помощью специально разработанных стилей.
type: docs
weight: 7340
url: /ru/net/aspose.words.themes/themefont/
---
## ThemeFont enumeration

Указывает типы названий шрифтов темы для тем документа.

```csharp
public enum ThemeFont
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Нет шрифта темы. |
| Major | `1` | Основной тематический шрифт. |
| Minor | `2` | Шрифт второстепенной темы. |

## Примечания

Указывает тип шрифта темы, на который можно ссылаться как на шрифт темы в свойствах родительского объекта. Этот шрифт темы является ссылкой на один из предопределенных шрифтов темы, расположенных в части документа Тема, которая позволяет централизованно устанавливать информацию о шрифте в документе.

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

Показывает, как работать со шрифтами и цветами темы.

```csharp
Document doc = new Document();

// Определить шрифты для языков, используемых по умолчанию.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Мы можем использовать шрифт и цвет темы вместо значений по умолчанию.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// Существует несколько способов сбросить шрифт и цвет.
// 1 - Устанавливая ThemeFont.None/ThemeColor.None:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - Задавая не относящиеся к теме названия шрифтов/цветов:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### Смотрите также

* пространство имен [Aspose.Words.Themes](../../aspose.words.themes/)
* сборка [Aspose.Words](../../)
