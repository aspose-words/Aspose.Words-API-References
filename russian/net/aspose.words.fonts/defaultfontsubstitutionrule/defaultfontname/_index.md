---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words для .NET
description: Узнайте, как легко управлять DefaultFontSubstitutionRule и настраивать имя шрифта по умолчанию для повышения гибкости дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Получает или задает имя шрифта по умолчанию.

```csharp
public string DefaultFontName { get; set; }
```

## Примечания

Значение по умолчанию — «Times New Roman».

## Примеры

Показывает, как установить правило замены шрифта по умолчанию.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Получить правило замены по умолчанию в FontSettings.
// Это правило заменит все отсутствующие шрифты на «Times New Roman».
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Установите замену шрифта по умолчанию на «Courier New».
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Используя конструктор документов, добавляем текст шрифтом, который нам не нужен, чтобы увидеть, как происходит замена,
// а затем визуализируем результат в формате PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

Показывает, как указать шрифт по умолчанию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Источники шрифтов, используемые в документе, содержат шрифт «Arial», но не «Arvo».
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Установите свойство "DefaultFontName" на "Courier New", чтобы,
// при визуализации документа применять этот шрифт во всех случаях, когда другой шрифт недоступен.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words теперь будет использовать шрифт по умолчанию вместо любых отсутствующих шрифтов во время любых вызовов рендеринга.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Смотрите также

* class [DefaultFontSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
