---
title: DownsampleOptions.DownsampleImages
linktitle: DownsampleImages
articleTitle: DownsampleImages
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „DownsampleImages“ die Bildqualität optimiert, indem sie das Downsampling für eine verbesserte Leistung und schnellere Ladezeiten steuert.
type: docs
weight: 20
url: /de/net/aspose.words.saving/downsampleoptions/downsampleimages/
---
## DownsampleOptions.DownsampleImages property

Gibt an, ob Bilder heruntergerechnet werden sollen.

```csharp
public bool DownsampleImages { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

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

* class [DownsampleOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
