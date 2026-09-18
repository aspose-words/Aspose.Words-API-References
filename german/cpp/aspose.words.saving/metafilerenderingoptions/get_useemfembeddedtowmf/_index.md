---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf Methode"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, wie WMF‑Metadateien mit eingebetteten EMF‑Metadateien in C++ gerendert werden sollen."
type: docs
weight: 7000
url: /de/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Liest oder legt einen Wert fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Hinweise


WMF‑Metadateien können eingebettete EMF‑Daten enthalten. MS Word verwendet in den meisten Fällen eingebettete EMF‑Daten. GDI+ verwendet immer WMF‑Daten.

Wenn dieser Wert auf **true** gesetzt ist, verwendet Aspose.Words beim Rendern eingebettete EMF‑Daten.

Wenn dieser Wert auf **false** gesetzt ist, verwendet Aspose.Words beim Rendern WMF‑Daten.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wird die Metadatei in ein Bitmap gerendert, werden immer WMF‑Daten verwendet.

Der Standardwert ist **true**.
## Siehe auch

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
