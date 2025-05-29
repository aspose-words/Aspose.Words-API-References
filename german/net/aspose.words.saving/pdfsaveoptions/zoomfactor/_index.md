---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words für .NET
description: Entdecken Sie die ZoomFactor-Eigenschaft von PdfSaveOptions, um die Zoomstufen von Dokumenten einfach in Prozent anzupassen und so Ihr PDF-Anzeigeerlebnis zu verbessern.
type: docs
weight: 360
url: /de/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Ruft einen Wert ab oder legt ihn fest, der den Zoomfaktor (in Prozent) für ein Dokument bestimmt.

```csharp
public int ZoomFactor { get; set; }
```

## Bemerkungen

Dieser Wert wird nur verwendet, wenn[`ZoomBehavior`](../zoombehavior/) ist eingestellt aufZoomFactor .

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

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
