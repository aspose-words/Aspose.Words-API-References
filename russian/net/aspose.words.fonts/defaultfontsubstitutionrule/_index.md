---
title: Class DefaultFontSubstitutionRule
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule сорт. Правило замены шрифта по умолчанию.
type: docs
weight: 2840
url: /ru/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Правило замены шрифта по умолчанию.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Получает или задает имя шрифта по умолчанию. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Указывает, включено правило или нет. |

### Примечания

Это правило определяет одно имя шрифта по умолчанию, которое будет использоваться для замены, если исходный шрифт недоступен.

### Примеры

Показывает, как установить правило замены шрифтов по умолчанию.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Получаем правило замены по умолчанию в FontSettings.
// Это правило заменит все отсутствующие шрифты на «Times New Roman».
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Установите замену шрифта по умолчанию на «Courier New».
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Используя конструктор документов, добавьте текст шрифтом, который нам не нужен, чтобы произошла замена,
// и затем визуализируем результат в PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Смотрите также

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


