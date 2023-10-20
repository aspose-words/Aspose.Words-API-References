---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words для .NET
description: Document FontSettings свойство. Получает или задает настройки шрифта документа на С#.
type: docs
weight: 140
url: /ru/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Получает или задает настройки шрифта документа.

```csharp
public FontSettings FontSettings { get; set; }
```

## Примечания

Это свойство позволяет указать настройки шрифта для каждого документа. Если установлено значение`нулевой` , настройки статического шрифта по умолчанию [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) будет использован.

Значение по умолчанию:`нулевой`.

## Примеры

Показывает, как настроить правила замены шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Источники шрифтов по умолчанию содержат первый шрифт, используемый в документе.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Второй шрифт «Аметиста» недоступен.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Мы можем настроить таблицу подстановки шрифтов, которая определяет
// какие шрифты Aspose.Words будет использовать в качестве замены недоступным шрифтам.
// Установите два шрифта-замены для «Аметисты»: «Арво» и «Курьер Новый».
// Если первая замена недоступна, Aspose.Words пытается использовать вторую замену и т.д.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // «Аметиста» недоступна, и правило замены гласит, что первым шрифтом, который будет использоваться в качестве замены, является «Арво».
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // «Арво» тоже нет, а «Курьер Новый» есть.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Выходной документ отобразит текст, использующий шрифт «Amethysta», отформатированный с помощью «Courier New».
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Смотрите также

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
