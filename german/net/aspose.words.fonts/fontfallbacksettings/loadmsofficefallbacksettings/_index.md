---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words für .NET
description: FontFallbackSettings LoadMsOfficeFallbackSettings methode. Lädt vordefinierte FallbackEinstellungen die den Microsoft WordFallback imitieren und Microsoft OfficeSchriftarten verwenden in C#.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Lädt vordefinierte Fallback-Einstellungen, die den Microsoft Word-Fallback imitieren und Microsoft Office-Schriftarten verwenden.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Beispiele

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
