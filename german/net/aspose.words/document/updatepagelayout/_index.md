---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words für .NET
description: Document UpdatePageLayout methode. Erstellt das Seitenlayout des Dokuments neu in C#.
type: docs
weight: 770
url: /de/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Erstellt das Seitenlayout des Dokuments neu.

```csharp
public void UpdatePageLayout()
```

## Bemerkungen

Diese Methode formatiert ein Dokument in Seiten und aktualisiert die seitenzahlbezogenen Felder im Dokument wie PAGE, PAGES, PAGEREF und REF. Die aktuellen Seitenlayoutinformationen sind für eine korrekte Darstellung des Dokuments in feste Seitenformate erforderlich.

Diese Methode wird automatisch aufgerufen, wenn Sie ein Dokument zum ersten Mal in PDF, XPS, Bild konvertieren oder drucken. Wenn Sie das Dokument jedoch nach dem Rendern ändern und dann versuchen, es erneut zu rendern, aktualisiert Aspose.Words das Seitenlayout nicht automatisch. In diesem Fall sollten Sie anrufen`UpdatePageLayout` before erneut rendern.

## Beispiele

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
