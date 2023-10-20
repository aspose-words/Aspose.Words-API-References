---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words für .NET
description: MetafileRenderingOptions UseGdiRasterOperationsEmulation eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob GDI für die Emulation von Rasteroperationen verwendet werden soll in C#.
type: docs
weight: 80
url: /de/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Bemerkungen

Die Windows GDI+-Bibliothek könnte zum Emulieren von Rasteroperationen verwendet werden. Im Vergleich zur Aspose.Words-eigenen Emulation bietet es Unterstützung für alle Rasteroperationen, die Leistung kann jedoch in einigen Fällen langsamer sein.

Wenn dieser Wert auf eingestellt ist`WAHR`, Aspose.Words verwendet GDI+ für die Emulation von Rasteroperationen.

Wenn dieser Wert auf eingestellt ist`FALSCH`Aspose.Words verwendet eine eigene Implementierung der Rasteroperationsemulation.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`FALSCH`.

## Beispiele

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

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
