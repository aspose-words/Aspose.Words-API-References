---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions‑Methode"
linktitle: "get_MetafileRenderingOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions‑Methode. Ermöglicht die Angabe, wie Metafiles in der gerenderten Ausgabe in C++ behandelt werden."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Ermöglicht die Angabe, wie Metadateien in der gerenderten Ausgabe behandelt werden.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Hinweise


Wenn [Vector](../../metafilerenderingmode/) angegeben ist, rendert Aspose.Words das Metafile zunächst zu Vektorgrafiken mit seiner eigenen Metafile‑Rendering‑Engine und rendert anschließend die Vektorgrafiken zum Bild.

Wenn [Bitmap](../../metafilerenderingmode/) angegeben ist, rendert Aspose.Words das Metafile direkt zum Bild mit der GDI+‑Metafile‑Rendering‑Engine.

Die GDI+‑Metafile‑Rendering‑Engine arbeitet schneller, unterstützt fast alle Metafile‑Funktionen, kann jedoch bei niedrigen Auflösungen im Vergleich zu den übrigen Vektorgrafiken (insbesondere bei Text) inkonsistente Ergebnisse liefern. Die Metafile‑Rendering‑Engine von Aspose.Words erzeugt selbst bei niedrigen Auflösungen konsistentere Ergebnisse, arbeitet jedoch langsamer und kann komplexe Metafiles ungenau rendern.

Der Standardwert für [MetafileRenderingMode](../../metafilerenderingmode/) ist [Bitmap](../../metafilerenderingmode/).

## Beispiele



Zeigt, wie man den Rendering‑Modus beim Speichern von Dokumenten mit Windows‑Metafile‑Bildern in andere Bildformate festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions‑Objekt übergeben, um
// Bestimmt, wie der Speichervorgang Windows‑Metafiles im Dokument verarbeitet.
// Wenn wir die Eigenschaft "RenderingMode" auf "MetafileRenderingMode.Vector" setzen,
// oder "MetafileRenderingMode.VectorWithFallback", rendern wir alle Metafiles als Vektorgrafiken.
// Wenn wir die Eigenschaft "RenderingMode" auf "MetafileRenderingMode.Bitmap" setzen, rendern wir alle Metafiles als Bitmaps.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words verwendet GDI+ zur Emulation von Rasteroperationen, wenn der Wert auf true gesetzt ist.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Siehe auch

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
