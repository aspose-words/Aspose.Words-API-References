---
title: Class DownsampleOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.DownsampleOptions klas. Ermöglicht die Angabe von DownsamplingOptionen.
type: docs
weight: 4970
url: /de/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Ermöglicht die Angabe von Downsampling-Optionen.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class DownsampleOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Gibt an, ob Bilder heruntergerechnet werden sollen. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder heruntergerechnet werden sollen. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Gibt die Schwellenwertauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument unter dem Schwellenwert liegt, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder dies tun können verkleinert werden, werden heruntergesampelt. |

### Beispiele

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Standardmäßig skaliert Aspose.Words alle Bilder in einem Dokument, das wir als PDF speichern, auf 220 ppi herunter.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Setzen Sie die Eigenschaft „Resolution“ auf „36“, um alle Bilder auf 36 ppi herunterzurechnen.
options.DownsampleOptions.Resolution = 36;

// Legen Sie die Eigenschaft „ResolutionThreshold“ so fest, dass nur das Downsampling angewendet wird
// Bilder mit einer Auflösung, die über 128 ppi liegt.
options.DownsampleOptions.ResolutionThreshold = 128;

// Nur die ersten beiden Bilder des Dokuments werden zu diesem Zeitpunkt heruntergerechnet.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


