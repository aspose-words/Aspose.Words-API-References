---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words für .NET
description: PdfSaveOptions InterpolateImages eigendom. Ein Flag das angibt ob die Bildinterpolation von einem konformen Lesegerät durchgeführt werden soll. WannFALSCH angegeben ist wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen wird das Standardverhalten des Readers verwendet in C#.
type: docs
weight: 210
url: /de/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Ein Flag, das angibt, ob die Bildinterpolation von einem konformen Lesegerät durchgeführt werden soll. Wann`FALSCH` angegeben ist, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen wird das Standardverhalten des Readers verwendet.

```csharp
public bool InterpolateImages { get; set; }
```

## Bemerkungen

Wenn die Auflösung eines Quellbilds deutlich niedriger ist als die des Ausgabegeräts, deckt jedes Quellbild viele Gerätepixel ab. Infolgedessen können Bilder zackig oder blockig erscheinen. Diese visuellen Artefakte können durch die Anwendung eines Bildinterpolationsalgorithmus während des Renderns reduziert werden. Anstatt alle von einem Quellmuster abgedeckten Pixel mit derselben Farbe zu malen, versucht die Bildinterpolation , eine Glättung zu erzeugen Übergang zwischen benachbarten Abtastwerten.

Ein konformer Leser kann sich dafür entscheiden, diese Funktion von PDF nicht zu implementieren, oder eine beliebige spezifische Implementierung der Interpolation verwenden, die er wünscht.

Der Standardwert ist`FALSCH`.

Das Interpolationsflag ist aufgrund der PDF/A-Konformität verboten.`FALSCH` Beim Speichern in PDF/A wird der Wert automatisch verwendet.

## Beispiele

Zeigt, wie man beim Speichern eines Dokuments als PDF eine Interpolation an Bildern durchführt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „InterpolateImages“ auf „true“, damit der Reader, der dieses Dokument öffnet, Bilder interpoliert.
// Ihre Auflösung sollte niedriger sein als die des Geräts, das das Dokument anzeigt.
// Setzen Sie die Eigenschaft „InterpolateImages“ auf „false“, damit der Reader keine Interpolation anwendet.
saveOptions.InterpolateImages = interpolateImages;

// Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, müssen wir das Bild vergrößern
// um den Interpolationseffekt zu sehen, wenn wir das Dokument mit aktivierter Funktion gespeichert haben.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

Zeigt, wie die Qualität eines Bildes in den gerenderten Dokumenten verbessert werden kann (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „InterpolateImages“ auf „true“, damit der Reader, der dieses Dokument öffnet, Bilder interpoliert.
// Ihre Auflösung sollte niedriger sein als die des Geräts, das das Dokument anzeigt.
// Setzen Sie die Eigenschaft „InterpolateImages“ auf „false“, damit der Reader keine Interpolation anwendet.
saveOptions.InterpolateImages = interpolateImages;

// Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, müssen wir das Bild vergrößern
// um den Interpolationseffekt zu sehen, wenn wir das Dokument mit aktivierter Funktion gespeichert haben.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
