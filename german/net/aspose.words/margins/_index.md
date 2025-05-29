---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Margins für anpassbare Dokumentränder. Verbessern Sie Ihre Dokumentformatierung mit benutzerfreundlichen Voreinstellungen!
type: docs
weight: 4580
url: /de/net/aspose.words/margins/
---
## Margins enumeration

Gibt voreingestellte Ränder an.

```csharp
public enum Margins
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | `0` | Normale Ränder. |
| Narrow | `1` | Schmale Ränder. |
| Moderate | `2` | Moderate Ränder. |
| Wide | `3` | Breite Ränder. |
| Mirrored | `4` | Gespiegelte Ränder. |
| Custom | `5` | Benutzerdefinierte Ränder. |

## Beispiele

Zeigt an, wann das Seitenlayout des Dokuments neu berechnet werden muss.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Das Speichern eines Dokuments als PDF, als Bild oder beim ersten Drucken wird automatisch
// Cachen Sie das Layout des Dokuments innerhalb seiner Seiten.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu erstellt
// das zwischengespeicherte Seitenlayout. Wenn wir das zwischengespeicherte Layout wünschen
// Um auf dem neuesten Stand zu bleiben, müssen wir es manuell aktualisieren.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
