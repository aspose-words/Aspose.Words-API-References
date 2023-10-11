---
title: Enum PdfZoomBehavior
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfZoomBehavior opsomming. Gibt den Zoomtyp an der auf ein PDFDokument angewendet wird wenn es in einem PDFViewer geöffnet wird.
type: docs
weight: 5540
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
| None | `0` | Wie das Dokument angezeigt wird, bleibt dem PDF-Viewer überlassen. Normalerweise zeigt der Viewer das Dokument so an, dass es der Seitenbreite entspricht. |
| ZoomFactor | `1` | Zeigt die Seite mit dem angegebenen Zoomfaktor an. |
| FitPage | `2` | Zeigt die Seite so an, dass sie vollständig sichtbar ist. |
| FitWidth | `3` | Passt sich der Breite der Seite an. |
| FitHeight | `4` | Passt sich der Höhe der Seite an. |
| FitBox | `5` | Passt in den Begrenzungsrahmen (Rechteck, das alle sichtbaren Elemente auf der Seite enthält). |

### Beispiele

Zeigt, wie der Standardzoom festgelegt wird, den ein Leser beim Öffnen eines gerenderten PDF-Dokuments anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie die Eigenschaft „ZoomBehavior“ auf „PdfZoomBehavior.ZoomFactor“, um einen PDF-Reader zu erhalten
// einen prozentualen Zoomfaktor anwenden, wenn wir das Dokument damit öffnen.
// Setzen Sie die Eigenschaft „ZoomFactor“ auf „25“, um dem Zoomfaktor einen Wert von 25 % zu geben.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, sehen wir das Dokument auf 1/4 seiner tatsächlichen Größe skaliert.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


