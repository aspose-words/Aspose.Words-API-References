---
title: PageSetup.Margins
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Gibt die Voreinstellung zurück oder legt sie festMargins der Seite.
type: docs
weight: 260
url: /de/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Gibt die Voreinstellung zurück oder legt sie fest[`Margins`](../../margins/) der Seite.

```csharp
public Margins Margins { get; set; }
```

### Beispiele

Zeigt an, wann das Seitenlayout des Dokuments neu berechnet werden soll.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Das Speichern eines Dokuments als PDF, ein Bild oder das erstmalige Drucken erfolgt automatisch
// Das Layout des Dokuments innerhalb seiner Seiten zwischenspeichern.
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
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


