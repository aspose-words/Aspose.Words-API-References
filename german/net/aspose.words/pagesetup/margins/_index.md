---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words für .NET
description: Passen Sie die Seitenränder mühelos mit der PageSetup-Eigenschaft an. Passen Sie die Einstellungen für optimales Layout und Präsentation an. Verbessern Sie das Erscheinungsbild Ihres Dokuments!
type: docs
weight: 260
url: /de/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Gibt die Voreinstellung zurück oder setzt sie[`Margins`](../../margins/) der Seite.

```csharp
public Margins Margins { get; set; }
```

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

* enum [Margins](../../margins/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
