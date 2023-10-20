---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words для .NET
description: FontSubstitutionSettings DefaultFontSubstitution свойство. Настройки относящиеся к правилу замены шрифтов по умолчанию на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Настройки, относящиеся к правилу замены шрифтов по умолчанию.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Примеры

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
