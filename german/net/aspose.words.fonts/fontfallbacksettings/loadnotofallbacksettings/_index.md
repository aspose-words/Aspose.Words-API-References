---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Ihre Typografie mit der FontFallbackSettings LoadNotoFallbackSettings-Methode verbessern können, indem Sie Google Noto-Schriftarten für eine nahtlose Textanzeige verwenden.
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

Zeigt, wie vordefinierte Fallback-Einstellungen für Google Noto-Schriftarten hinzugefügt werden.

```csharp
FontSettings fontSettings = new FontSettings();

// Dies sind kostenlose Schriftarten, die unter der SIL Open Font License lizenziert sind.
// Die Schriftarten können wir hier herunterladen:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

    // Beachten Sie, dass die vordefinierten Einstellungen nur Noto-Schriftarten im Sans-Stil mit normaler Stärke verwenden.
// Einige der Noto-Schriftarten verwenden erweiterte Typografiefunktionen.
// Schriftarten mit erweiterter Typografie werden möglicherweise nicht richtig wiedergegeben, da Aspose.Words diese derzeit nicht unterstützt.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Zeigt, wie vordefinierte Fallback-Schriftarteneinstellungen geladen werden.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Speichern Sie das standardmäßige Fallback-Schriftschema in einem XML-Dokument.
// Beispielsweise hat eines der Elemente einen Wert von „0C00-0C7F“ für Range und einen entsprechenden „Vani“-Wert für FallbackFonts.
// Dies bedeutet, dass, wenn die Schriftart, die für einen Text verwendet wird, keine Symbole für den Unicode-Block 0x0C00-0x0C7F hat,
// Das Fallback-Schema verwendet Symbole aus dem Schriftartenersatz „Vani“.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Unten sind zwei vordefinierte Schriftart-Fallback-Schemata aufgeführt, aus denen wir auswählen können.
// 1 - Verwenden Sie das Standardschema von Microsoft Office, das mit dem Standard identisch ist:
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
