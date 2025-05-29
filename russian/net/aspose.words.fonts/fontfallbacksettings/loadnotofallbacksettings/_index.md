---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words для .NET
description: Узнайте, как улучшить типографику с помощью метода FontFallbackSettings LoadNotoFallbackSettings, используя шрифты Google Noto для бесшовного отображения текста.
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Загружает предопределенные резервные настройки, которые используют шрифты Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

## Примеры

Показывает, как добавить предопределенные настройки резервного шрифта для шрифтов Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// Это бесплатные шрифты, лицензированные по лицензии SIL Open Font License.
// Шрифты можно скачать здесь:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Обратите внимание, что предустановленные настройки используют только шрифты Noto в стиле Sans с обычной толщиной.
// Некоторые шрифты Noto используют расширенные возможности типографики.
// Шрифты с расширенной типографикой могут отображаться некорректно, поскольку Aspose.Words в настоящее время их не поддерживает.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

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
