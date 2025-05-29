---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words для .NET
description: Откройте для себя метод FontFallbackSettings LoadMsOfficeFallbackSettings, позволяющий легко реализовать резервные настройки в стиле Microsoft Word со шрифтами Office для бесшовной интеграции.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Загружает предопределенные резервные настройки, которые имитируют резервные настройки Microsoft Word и используют шрифты Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Примеры

Показывает, как загрузить предопределенные резервные настройки шрифта.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Сохраните резервную схему шрифтов по умолчанию в XML-документе.
// Например, один из элементов имеет значение «0C00-0C7F» для Range и соответствующее значение «Vani» для FallbackFonts.
// Это означает, что если шрифт, используемый в тексте, не имеет символов для блока Unicode 0x0C00-0x0C7F,
// резервная схема будет использовать символы из заменителя шрифта "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Ниже приведены две предопределенные схемы резервного шрифта, из которых мы можем выбирать.
// 1 — Использовать схему Microsoft Office по умолчанию, которая совпадает со схемой по умолчанию:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Использовать схему, созданную на основе шрифтов Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Смотрите также

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
