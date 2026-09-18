---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations Methode"
linktitle: "get_EmulateRasterOperations"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob Rasteroperationen in C++ emuliert werden sollen oder nicht."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Liest oder legt einen Wert fest, der bestimmt, ob Rasteroperationen emuliert werden sollen oder nicht.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Hinweise


Spezifische Rasteroperationen können in Metadateien verwendet werden. Sie können nicht direkt in Vektorgrafiken gerendert werden. Das Emulieren von Rasteroperationen erfordert eine teilweise Rasterisierung der resultierenden Vektorgrafiken, was die Rendering‑Leistung der Metadatei beeinträchtigen kann.

Wenn dieser Wert auf **true** gesetzt ist, emuliert Aspose.Words die Rasteroperationen. Das resultierende Ergebnis kann teilweise rasterisiert sein und die Leistung könnte langsamer sein.

Wenn dieser Wert auf **false** gesetzt ist, emuliert Aspose.Words die Rasteroperationen nicht. Wenn [Aspose.Words](../../../aspose.words/) in einer Metadatei eine Rasteroperation erkennt, greift es auf die Darstellung der Metadatei in ein Bitmap zurück, indem das Betriebssystem verwendet wird.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist **true**.
## Siehe auch

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
