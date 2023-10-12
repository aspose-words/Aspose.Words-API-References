---
title: DownsampleOptions.ResolutionThreshold
second_title: Aspose.Words für .NET-API-Referenz
description: DownsampleOptions eigendom. Gibt die Schwellenwertauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument unter dem Schwellenwert liegt wird der DownsamplingAlgorithmus nicht angewendet. Ein Wert von 0 bedeutet dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder dies tun können verkleinert werden werden heruntergesampelt.
type: docs
weight: 40
url: /de/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Gibt die Schwellenwertauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument unter dem Schwellenwert liegt, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder dies tun können verkleinert werden, werden heruntergesampelt.

```csharp
public int ResolutionThreshold { get; set; }
```

### Bemerkungen

Der Standardwert ist 0.

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

* class [DownsampleOptions](../)
* namensraum [Aspose.Words.Saving](../../downsampleoptions/)
* Montage [Aspose.Words](../../../)


