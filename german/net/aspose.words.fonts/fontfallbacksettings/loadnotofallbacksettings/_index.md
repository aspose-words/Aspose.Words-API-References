---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words für .NET
description: FontFallbackSettings LoadNotoFallbackSettings methode. Lädt vordefinierte FallbackEinstellungen die Google NotoSchriftarten verwenden in C#.
type: docs
weight: 40
url: /de/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Lädt vordefinierte Fallback-Einstellungen, die Google Noto-Schriftarten verwenden.

```csharp
public void LoadNotoFallbackSettings()
```

## Beispiele

Zeigt, wie man vordefinierte Schriftart-Fallback-Einstellungen für Google Noto-Schriftarten hinzufügt.

```csharp
FontSettings fontSettings = new FontSettings();

// Dies sind kostenlose Schriftarten, die unter der SIL Open Font License lizenziert sind.
// Die Schriftarten können wir hier herunterladen:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Beachten Sie, dass in den vordefinierten Einstellungen nur Noto-Schriftarten im Sans-Stil mit normaler Stärke verwendet werden.
// Einige der Noto-Schriftarten verwenden erweiterte Typografiefunktionen.
// Schriftarten mit erweiterter Typografie werden möglicherweise nicht korrekt wiedergegeben, da Aspose.Words sie derzeit nicht unterstützt.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Zeigt, wie vordefinierte Fallback-Schriftarteinstellungen geladen werden.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Speichern Sie das Standard-Fallback-Schriftartschema in einem XML-Dokument.
// Beispielsweise hat eines der Elemente den Wert „0C00-0C7F“ für Range und einen entsprechenden „Vani“-Wert für FallbackFonts.
// Dies bedeutet, dass, wenn die Schriftart, die ein Text verwendet, keine Symbole für den Unicode-Block 0x0C00-0x0C7F enthält,
// Das Fallback-Schema verwendet Symbole aus der Schriftart „Vani“.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Nachfolgend finden Sie zwei vordefinierte Schriftart-Fallback-Schemata, aus denen wir wählen können.
// 1 – Verwenden Sie das Standardschema von Microsoft Office, das mit dem Standardschema identisch ist:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 – Verwenden Sie das aus Google Noto-Schriftarten erstellte Schema:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Siehe auch

* class [FontFallbackSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
