---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die DownsampleOptions-Eigenschaft von PdfSaveOptions, um Ihre PDF-Qualität anzupassen und die Dateigröße für bessere Leistung und Klarheit zu optimieren.
type: docs
weight: 110
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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
