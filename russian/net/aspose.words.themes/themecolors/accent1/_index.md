---
title: ThemeColors.Accent1
second_title: Справочник по API Aspose.Words для .NET
description: ThemeColors свойство. Определяет цветовой акцент 1.
type: docs
weight: 10
url: /ru/net/aspose.words.themes/themecolors/accent1/
---
## ThemeColors.Accent1 property

Определяет цветовой акцент 1.

```csharp
public Color Accent1 { get; set; }
```

### Примеры

Показывает, как устанавливать собственные цвета и шрифты для тем.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Объект «Тема» дает нам доступ к теме документа, источнику шрифтов и цветов по умолчанию.
Theme theme = doc.Theme;

// Некоторые стили, такие как «Заголовок 1» и «Подзаголовок», наследуют эти шрифты.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Другие языки также могут иметь свои собственные шрифты в этой теме.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Свойство "Цвета" содержит цветовую палитру из Microsoft Word,
// который появляется при изменении заливки или цвета шрифта.
// Применяем пользовательские цвета к цветовой палитре, чтобы иметь к ним легкий доступ в Microsoft Word
// когда мы, например, меняем цвет шрифта через "Домой" -> gt; «Шрифт» -> "Цвет шрифта",
// или вставьте фигуру, а затем задайте для нее цвет с помощью «Формата фигуры» -> gt; «Стили фигур».
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// Применяем пользовательские цвета к гиперссылкам в состояниях, когда они нажаты и не нажаты.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Смотрите также

* class [ThemeColors](../)
* пространство имен [Aspose.Words.Themes](../../themecolors/)
* сборка [Aspose.Words](../../../)


