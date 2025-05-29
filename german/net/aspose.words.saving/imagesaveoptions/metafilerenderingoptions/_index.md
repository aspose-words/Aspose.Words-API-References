---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ImageSaveOptions MetafileRenderingOptions“, um die Metadateiverarbeitung in Ihrer gerenderten Ausgabe für eine verbesserte Bildqualität zu steuern.
type: docs
weight: 90
url: /de/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Ermöglicht die Angabe, wie Metadateien in der gerenderten Ausgabe behandelt werden.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Bemerkungen

WannVector angegeben ist, rendert Aspose.Words zuerst die x000d_-Metadatei mithilfe seiner eigenen Metadatei-Rendering-Engine in Vektorgrafiken und rendert dann die x000d_-Vektorgrafiken in das Bild.

WannBitmap angegeben ist, rendert Aspose.Words die Metadatei mithilfe der GDI+-Metadatei-Rendering-Engine direkt in das Bild.

Die GDI+-Metadatei-Rendering-Engine arbeitet schneller und unterstützt fast alle Metadatei-Funktionen, kann aber bei niedrigen Auflösungen zu inkonsistenten Ergebnissen im Vergleich zu den übrigen Vektorgrafiken (insbesondere für Text) auf der Seite führen. Die Aspose.Words-Metadatei-Rendering-Engine liefert auch bei niedrigen Auflösungen konsistentere Ergebnisse, arbeitet aber langsamer und kann komplexe Metadateien ungenau rendern.

Der Standardwert für[`MetafileRenderingMode`](../../metafilerenderingmode/) IstBitmap.

## Beispiele

Zeigt, wie der Renderingmodus beim Speichern von Dokumenten mit Windows-Metafile-Bildern in anderen Bildformaten eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Bestimmen Sie, wie der Speichervorgang Windows-Metadateien im Dokument verarbeitet.
// Wenn wir die Eigenschaft "RenderingMode" auf "MetafileRenderingMode.Vector" setzen,
// oder „MetafileRenderingMode.VectorWithFallback“, wir rendern alle Metadateien als Vektorgrafiken.
// Wenn wir die Eigenschaft „RenderingMode“ auf „MetafileRenderingMode.Bitmap“ setzen, rendern wir alle Metadateien als Bitmaps.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words verwendet GDI+ zur Emulation von Rasteroperationen, wenn der Wert auf „true“ gesetzt ist.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Siehe auch

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
