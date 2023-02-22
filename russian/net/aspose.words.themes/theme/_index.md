---
title: Class Theme
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Themes.Theme сорт. Представляет тему документа и обеспечивает доступ к основным частям темы включаяMajorFonts MinorFonts а такжеColors
type: docs
weight: 6160
url: /ru/net/aspose.words.themes/theme/
---
## Theme class

Представляет тему документа и обеспечивает доступ к основным частям темы, включая[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) а также[`Colors`](./colors/)

```csharp
public class Theme
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Theme](theme/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Позволяет указать набор цветов темы для документа. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Позволяет указать набор основных шрифтов для разных языков. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Позволяет указать набор минорных шрифтов для разных языков. |

### Примеры

Показывает, как установить пользовательские цвета и шрифты для тем.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Объект «Тема» дает нам доступ к теме документа, источнику шрифтов и цветов по умолчанию.
Theme theme = doc.Theme;

// Некоторые стили, такие как «Заголовок 1» и «Подзаголовок», наследуют эти шрифты.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Другие языки также могут иметь собственные шрифты в этой теме.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Свойство "Цвета" содержит цветовую палитру из Microsoft Word,
// который появляется при изменении оттенка или цвета шрифта.
// Применение пользовательских цветов к цветовой палитре, чтобы у нас был легкий доступ к ним в Microsoft Word
// когда мы, например, меняем цвет шрифта через "Home" -> "Шрифт" -> "Цвет шрифта",
// или вставьте фигуру, а затем установите для нее цвет через "Формат фигуры" -> «Стили фигур».
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

// Применяем пользовательские цвета к гиперссылкам в состоянии нажатия и отсутствия щелчка.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Themes](../../aspose.words.themes/)
* сборка [Aspose.Words](../../)


