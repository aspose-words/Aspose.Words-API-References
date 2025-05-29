---
title: ThemeColors.Dark1
linktitle: Dark1
articleTitle: Dark1
second_title: Aspose.Words для .NET
description: Откройте для себя ThemeColors Dark1 для яркой цветовой палитры. Улучшите свои проекты с помощью этого универсального оттенка Dark 1 для современной эстетики.
type: docs
weight: 70
url: /ru/net/aspose.words.themes/themecolors/dark1/
---
## ThemeColors.Dark1 property

Определяет цвет Темный 1.

```csharp
public Color Dark1 { get; set; }
```

## Примеры

Показывает, как устанавливать пользовательские цвета и шрифты для тем.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Объект «Тема» предоставляет нам доступ к теме документа, источнику шрифтов и цветов по умолчанию.
Theme theme = doc.Theme;

// Некоторые стили, такие как «Заголовок 1» и «Подзаголовок», унаследуют эти шрифты.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Другие языки также могут иметь свои собственные шрифты в этой теме.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Свойство «Цвета» содержит цветовую палитру из Microsoft Word,
// который появляется при изменении затенения или цвета шрифта.
// Применяем пользовательские цвета к цветовой палитре, чтобы иметь к ним легкий доступ в Microsoft Word
// когда мы, например, меняем цвет шрифта через "Главная" -> "Шрифт" -> "Цвет шрифта",
// или вставьте фигуру, а затем задайте для нее цвет с помощью «Формат фигуры» -> «Стили фигуры».
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

// Применить пользовательские цвета к гиперссылкам в нажатом и ненажатом состоянии.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Смотрите также

* class [ThemeColors](../)
* пространство имен [Aspose.Words.Themes](../../../aspose.words.themes/)
* сборка [Aspose.Words](../../../)
