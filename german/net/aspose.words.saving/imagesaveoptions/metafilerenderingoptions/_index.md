---
title: ImageSaveOptions.MetafileRenderingOptions
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ermöglicht die Angabe wie Metadateien in der gerenderten Ausgabe behandelt werden.
type: docs
weight: 90
url: /de/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Ermöglicht die Angabe, wie Metadateien in der gerenderten Ausgabe behandelt werden.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

### Bemerkungen

WannVector angegeben ist, rendert Aspose.Words zunächst die Metadatei in Vektorgrafiken mithilfe seiner eigenen Metadatei-Rendering-Engine und rendert dann die Metadatei vector in das Bild.

WannBitmap angegeben ist, rendert Aspose.Words die Metadatei mithilfe der GDI+-Metadatei-Rendering-Engine direkt in das Bild.

Die GDI+-Metadatei-Rendering-Engine arbeitet schneller und unterstützt fast alle Metadateifunktionen. Bei niedrigen -Auflösungen kann es jedoch zu inkonsistenten Ergebnissen im Vergleich zu den übrigen Vektorgrafiken (insbesondere für Text) auf der Seite kommen. Die Metadatei-Rendering-Engine von Aspose.Words liefert sogar bei niedrigen Auflösungen konsistentere Ergebnisse, arbeitet jedoch langsamer und rendert möglicherweise komplexe Metadateien ungenau.

Der Standardwert für[`MetafileRenderingMode`](../../metafilerenderingmode/) IstBitmap.

### Beispiele

Zeigt, wie der Rendering-Modus beim Speichern von Dokumenten mit Windows Metafile-Bildern in anderen Bildformaten festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
// Bestimmen Sie, wie der Speichervorgang Windows-Metadateien im Dokument verarbeitet.
// Wenn wir die Eigenschaft „RenderingMode“ auf „MetafileRenderingMode.Vector“ setzen,
// oder „MetafileRenderingMode.VectorWithFallback“, wir rendern alle Metadateien als Vektorgrafiken.
// Wenn wir die Eigenschaft „RenderingMode“ auf „MetafileRenderingMode.Bitmap“ setzen, rendern wir alle Metadateien als Bitmaps.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words verwendet GDI+ für die Emulation von Rasteroperationen, wenn der Wert auf „true“ gesetzt ist.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Siehe auch

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


