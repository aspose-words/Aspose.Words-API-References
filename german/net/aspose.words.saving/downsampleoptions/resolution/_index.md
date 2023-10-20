---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words für .NET
description: DownsampleOptions Resolution eigendom. Gibt die Auflösung in Pixel pro Zoll an auf die die Bilder heruntergerechnet werden sollen in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder heruntergerechnet werden sollen.

```csharp
public int Resolution { get; set; }
```

## Bemerkungen

Der Standardwert ist 220 ppi.

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

* class [DownsampleOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
