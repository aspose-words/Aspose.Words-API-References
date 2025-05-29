---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.PdfZoomBehavior-Aufzählung für anpassbare PDF-Zoomeinstellungen. Verbessern Sie das Benutzererlebnis mit maßgeschneiderten Anzeigeoptionen in PDF-Dokumenten.
type: docs
weight: 6340
url: /de/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Gibt den Zoomtyp an, der auf ein PDF-Dokument angewendet wird, wenn es in einem PDF-Viewer geöffnet wird.

```csharp
public enum PdfZoomBehavior
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Die Anzeige des Dokuments wird dem PDF-Viewer überlassen. Normalerweise wird das Dokument seitenbreitengerecht angezeigt. |
| ZoomFactor | `1` | Zeigt die Seite mit dem angegebenen Zoomfaktor an. |
| FitPage | `2` | Zeigt die Seite so an, dass sie vollständig sichtbar ist. |
| FitWidth | `3` | Passt sich der Breite der Seite an. |
| FitHeight | `4` | Passt sich der Höhe der Seite an. |
| FitBox | `5` | Passt den Begrenzungsrahmen an (Rechteck, das alle sichtbaren Elemente auf der Seite enthält). |

## Beispiele

Zeigt, wie der Standardzoom festgelegt wird, den ein Reader beim Öffnen eines gerenderten PDF-Dokuments anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie die Eigenschaft "ZoomBehavior" auf "PdfZoomBehavior.ZoomFactor", um einen PDF-Reader zu erhalten
// wenden Sie einen prozentualen Zoomfaktor an, wenn wir das Dokument damit öffnen.
// Setzen Sie die Eigenschaft „ZoomFactor“ auf „25“, um dem Zoomfaktor einen Wert von 25 % zuzuweisen.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, wird das Dokument auf 1/4 seiner tatsächlichen Größe skaliert angezeigt.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
