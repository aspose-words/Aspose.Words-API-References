---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words für .NET
description: Entdecken Sie die InterpolateImages-Eigenschaft von PdfSaveOptions, eine wichtige Funktion zur Verbesserung der Bildqualität in Ihren Dokumenten. Optimieren Sie Ihre PDFs mühelos!
type: docs
weight: 210
url: /de/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Ein Flag, das angibt, ob die Bildinterpolation von einem konformen Reader durchgeführt werden soll. Wenn`FALSCH` angegeben ist, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen wird das Standardverhalten des Readers verwendet.

```csharp
public bool InterpolateImages { get; set; }
```

## Bemerkungen

Wenn die Auflösung eines Quellbildes deutlich niedriger ist als die des Ausgabegeräts, deckt jedes Quellbild viele Gerätepixel ab. Dadurch können Bilder zackig oder blockartig wirken. Diese visuellen Artefakte lassen sich durch die Anwendung eines Bildinterpolationsalgorithmus während des Renderns reduzieren. Anstatt alle Pixel eines Quellbilds mit derselben Farbe zu übermalen, versucht die Bildinterpolation, einen sanften Übergang zwischen benachbarten Bildwerten zu erzeugen.

Ein konformer Reader kann sich dafür entscheiden, diese Funktion von PDF nicht zu implementieren, oder eine beliebige spezifische Interpolationsimplementierung verwenden.

Der Standardwert ist`FALSCH`.

Interpolationsflag ist durch die PDF/A-Konformität verboten.`FALSCH` Beim Speichern im PDF/A-Format wird der Wert automatisch verwendet.

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im PDF-Format eine Interpolation an Bildern durchgeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Setzen Sie die Eigenschaft „InterpolateImages“ auf „true“, damit der Reader, der dieses Dokument öffnet, Bilder interpoliert.
// Ihre Auflösung sollte niedriger sein als die des Geräts, auf dem das Dokument angezeigt wird.
// Setzen Sie die Eigenschaft „InterpolateImages“ auf „false“, damit der Reader keine Interpolation anwendet.
saveOptions.InterpolateImages = interpolateImages;

// Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, müssen wir das Bild vergrößern
// um den Interpolationseffekt zu sehen, wenn wir das Dokument mit aktivierter Interpolation gespeichert haben.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
