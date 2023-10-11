---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
second_title: Справочник по API Aspose.Words для .NET
description: FontFallbackSettings метод. Загружает предопределенные резервные настройки которые имитируют резервный вариант Microsoft Word и используют шрифты Microsoft Office.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Загружает предопределенные резервные настройки, которые имитируют резервный вариант Microsoft Word и используют шрифты Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

### Примеры

Показывает, как загрузить предварительно определенные настройки резервного шрифта.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Сохраняем схему резервного шрифта по умолчанию в XML-документ.
// Например, один из элементов имеет значение «0C00-0C7F» для Range и соответствующее значение «Vani» для FallbackFonts.
// Это означает, что если шрифт, используемый в каком-либо тексте, не содержит символов для блока Юникода 0x0C00-0x0C7F,
// в резервной схеме будут использоваться символы из заменителя шрифта "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Ниже приведены две предопределенные схемы резервного шрифта, которые мы можем выбрать.
// 1 — использовать схему Microsoft Office по умолчанию, аналогичную схеме по умолчанию:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 — Использовать схему, построенную на основе шрифтов Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Смотрите также

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../fontfallbacksettings/)
* сборка [Aspose.Words](../../../)


