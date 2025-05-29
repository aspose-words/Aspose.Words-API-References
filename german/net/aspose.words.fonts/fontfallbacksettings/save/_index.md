---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words für .NET
description: Speichern Sie Ihre FontFallbackSettings mühelos mit unserer intuitiven Speichermethode. Bewahren Sie Ihre benutzerdefinierten Fallback-Einstellungen für eine nahtlose Schriftverwaltung.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Speichert die aktuellen Fallback-Einstellungen im Stream.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Ausgabestream. |

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

---

## Save(*string*) {#save_1}

Speichert die aktuellen Fallback-Einstellungen in einer Datei.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Ausgabedatei. |

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
