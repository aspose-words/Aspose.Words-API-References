---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words für .NET
description: FontFallbackSettings Load methode. Lädt SchriftartFallbackEinstellungen aus der XMLDatei in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Lädt Schriftart-Fallback-Einstellungen aus der XML-Datei.

```csharp
public void Load(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Eingabedatei. |

## Beispiele

Zeigt, wie Schriftart-Fallback-Einstellungen in/aus einem XML-Dokument im lokalen Dateisystem geladen und gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laden Sie ein XML-Dokument, das eine Reihe von Schriftart-Fallback-Einstellungen definiert.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Speichern Sie die aktuellen Schriftart-Fallback-Einstellungen unseres Dokuments als XML-Dokument.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Siehe auch

* class [FontFallbackSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

Lädt Fallback-Einstellungen aus dem XML-Stream.

```csharp
public void Load(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Eingabestrom. |

## Beispiele

Zeigt, wie Schriftart-Fallback-Einstellungen in/aus einem Stream geladen und gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laden Sie ein XML-Dokument, das eine Reihe von Schriftart-Fallback-Einstellungen definiert.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Verwenden Sie einen Stream, um die aktuellen Schriftart-Fallback-Einstellungen unseres Dokuments als XML-Dokument zu speichern.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Siehe auch

* class [FontFallbackSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
