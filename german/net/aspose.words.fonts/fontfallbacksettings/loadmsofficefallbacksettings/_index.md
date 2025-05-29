---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode FontFallbackSettings LoadMsOfficeFallbackSettings, um Microsoft Word-ähnliche Fallback-Einstellungen mit Office-Schriftarten für eine nahtlose Integration einfach zu implementieren.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Lädt vordefinierte Fallback-Einstellungen, die den Fallback von Microsoft Word nachahmen und Microsoft Office-Schriftarten verwenden.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Beispiele

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
