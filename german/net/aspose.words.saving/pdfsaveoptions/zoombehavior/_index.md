---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words für .NET
description: Entdecken Sie PdfSaveOptions ZoomBehavior und steuern Sie die Zoomeinstellungen für eine optimale Anzeige in PDF-Viewern. Verbessern Sie die Benutzerfreundlichkeit mit maßgeschneiderter Dokumentanzeige!
type: docs
weight: 350
url: /de/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, welche Art von Zoom angewendet werden soll, wenn ein Dokument mit einem PDF-Viewer geöffnet wird.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Bemerkungen

Der Standardwert istNone , d. h. es wird keine Anpassung angewendet.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
