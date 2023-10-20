---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words für .NET
description: PdfSaveOptions DownsampleOptions eigendom. Ermöglicht die Angabe von DownsamplingOptionen in C#.
type: docs
weight: 100
url: /de/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Ermöglicht die Angabe von Downsampling-Optionen.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

## Beispiele

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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
