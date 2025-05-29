---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Bilder mit der Eigenschaft „DownsampleOptions ResolutionThreshold“. Steuern Sie das Downsampling basierend auf der Auflösung für bessere Leistung und Qualität.
type: docs
weight: 40
url: /de/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Gibt die Schwellenauflösung in Pixeln pro Zoll an. Wenn die Auflösung eines Bildes im Dokument kleiner als der Schwellenwert ist, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder, deren Größe reduziert werden kann, heruntergerechnet werden.

```csharp
public int ResolutionThreshold { get; set; }
```

## Bemerkungen

Der Standardwert ist 0.

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
