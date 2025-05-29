---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words für .NET
description: Laden und verwalten Sie mühelos Fallback-Einstellungen für Schriftarten aus XML-Dateien mit der Lademethode „FontFallbackSettings“ für eine nahtlose Typografieintegration.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Lädt die Fallback-Einstellungen für Schriftarten aus einer XML-Datei.

```csharp
public void Load(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Geben Sie den Dateinamen ein. |

## Beispiele

Zeigt, wie Sie Schriftart-Fallback-Einstellungen in ein/aus einem XML-Dokument im lokalen Dateisystem laden und speichern.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laden Sie ein XML-Dokument, das eine Reihe von Fallback-Schriftarteneinstellungen definiert.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Speichern Sie die aktuellen Fallback-Schriftarteneinstellungen unseres Dokuments als XML-Dokument.
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
| stream | Stream | Eingabestream. |

## Beispiele

Zeigt, wie Schriftart-Fallback-Einstellungen in einen/aus einem Stream geladen und gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laden Sie ein XML-Dokument, das eine Reihe von Fallback-Schriftarteneinstellungen definiert.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Verwenden Sie einen Stream, um die aktuellen Fallback-Einstellungen für die Schriftart unseres Dokuments als XML-Dokument zu speichern.
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
