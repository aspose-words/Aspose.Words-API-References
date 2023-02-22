---
title: DownsampleOptions.ResolutionThreshold
second_title: Aspose.Words für .NET-API-Referenz
description: DownsampleOptions eigendom. Gibt die Schwellenauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument unter dem Schwellenwert liegt wird der DownsamplingAlgorithmus nicht angewendet. Ein Wert von 0 bedeutet dass die Schwellenprüfung nicht verwendet wird und alle Bilder verkleinert werden können werden heruntergesampelt.
type: docs
weight: 40
url: /de/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Gibt die Schwellenauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument unter dem Schwellenwert liegt, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenprüfung nicht verwendet wird und alle Bilder verkleinert werden können, werden heruntergesampelt.

```csharp
public int ResolutionThreshold { get; set; }
```

### Bemerkungen

Der Standardwert ist 0.

### Beispiele

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Standardmäßig verkleinert Aspose.Words alle Bilder in einem Dokument, das wir als PDF speichern, auf 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Setzen Sie die Eigenschaft "Auflösung" auf "36", um alle Bilder auf 36 ppi herunterzurechnen.
options.DownsampleOptions.Resolution = 36;

// Legen Sie die Eigenschaft "ResolutionThreshold" fest, um nur das Downsampling anzuwenden
// Bilder mit einer Auflösung von über 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Zu diesem Zeitpunkt werden nur die ersten beiden Bilder des Dokuments heruntergerechnet.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Siehe auch

* class [DownsampleOptions](../)
* namensraum [Aspose.Words.Saving](../../downsampleoptions/)
* Montage [Aspose.Words](../../../)


