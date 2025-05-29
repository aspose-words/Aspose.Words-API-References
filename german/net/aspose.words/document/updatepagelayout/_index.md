---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words für .NET
description: Überarbeiten Sie die Struktur Ihres Dokuments mit der Methode UpdatePageLayout und sorgen Sie für ein ansprechendes und übersichtliches Layout zur Verbesserung der Lesbarkeit und Präsentation.
type: docs
weight: 830
url: /de/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Erstellt das Seitenlayout des Dokuments neu.

```csharp
public void UpdatePageLayout()
```

## Bemerkungen

Diese Methode formatiert ein Dokument in Seiten und aktualisiert die seitenbezogenen Felder im Dokument, z. B. PAGE, PAGES, PAGEREF und REF. Die aktuellen Seitenlayoutinformationen sind für die korrekte Darstellung des Dokuments in festen Seitenformaten erforderlich.

Diese Methode wird automatisch aufgerufen, wenn Sie ein Dokument zum ersten Mal in PDF, XPS, Bild oder beim Drucken konvertieren. Wenn Sie das Dokument jedoch nach dem Rendern ändern und dann erneut versuchen, es zu rendern, aktualisiert Aspose.Words das Seitenlayout nicht automatisch. In diesem Fall sollten Sie Folgendes aufrufen:`UpdatePageLayout` before erneut rendern.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
