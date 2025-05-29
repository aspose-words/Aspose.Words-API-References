---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.DownsampleOptions, um das Downsampling von Bildern für eine optimierte Dokumentqualität und Leistung einfach anzupassen.
type: docs
weight: 5720
url: /de/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Ermöglicht die Angabe von Downsampling-Optionen.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

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
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Gibt die Auflösung in Pixeln pro Zoll an, auf die die Bilder heruntergerechnet werden sollen. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Gibt die Schwellenauflösung in Pixeln pro Zoll an. Wenn die Auflösung eines Bildes im Dokument kleiner als der Schwellenwert ist, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder, deren Größe reduziert werden kann, heruntergerechnet werden. |

## Beispiele

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Standardmäßig reduziert Aspose.Words alle Bilder in einem Dokument, das wir als PDF speichern, auf 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Setzen Sie die Eigenschaft „Auflösung“ auf „36“, um alle Bilder auf 36 ppi herunterzurechnen.
options.DownsampleOptions.Resolution = 36;

// Setzen Sie die Eigenschaft "ResolutionThreshold", um das Downsampling nur auf
// Bilder mit einer Auflösung über 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// In dieser Phase werden nur die ersten beiden Bilder des Dokuments heruntergerechnet.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
