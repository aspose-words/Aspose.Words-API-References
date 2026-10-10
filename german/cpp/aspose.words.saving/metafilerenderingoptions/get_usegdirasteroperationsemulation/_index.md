---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation Methode"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen in C++ verwendet wird."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Liest oder legt einen Wert fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Hinweise


Die Windows GDI+-Bibliothek kann verwendet werden, um Rasteroperationen zu emulieren. Sie bietet Unterstützung für alle Rasteroperationen im Vergleich zur eigenen Emulation von Aspose.Words, jedoch kann die Leistung in einigen Fällen langsamer sein.

Wenn dieser Wert auf **true** gesetzt ist, verwendet Aspose.Words GDI+ für die Emulation von Rasteroperationen.

Wenn dieser Wert auf **false** gesetzt ist, verwendet Aspose.Words seine eigene Implementierung der Emulation von Rasteroperationen.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist **false**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
