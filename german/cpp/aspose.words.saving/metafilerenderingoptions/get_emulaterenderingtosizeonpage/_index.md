---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage Methode"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob das Rendering der Metadatei die Anzeige der Metadatei gemäß der Größe auf der Seite nachahmt oder die Anzeige der Metadatei in ihrer Standardgröße in C++."
type: docs
weight: 4334
url: /de/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Liest oder legt einen Wert fest, der bestimmt, ob das Metafile-Rendering die Anzeige des Metafiles gemäß der Größe auf der Seite oder in seiner Standardgröße emuliert.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Hinweise


Wenn Metadateien in MS Word angezeigt werden, können einige Grafiken gemäß der tatsächlichen Metadateigröße in Pixeln skaliert werden. Das heißt, selbst das Zoomen kann die Anzeige der Metadatei beeinflussen.

Wenn dieser Wert auf **true** gesetzt ist, emuliert Aspose.Words das Rendern gemäß der Metadateigröße auf der Seite. Die Größe in Pixeln wird aus der Metadateigröße auf der Seite und der angegebenen [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) berechnet.

Wenn dieser Wert auf **false** gesetzt ist, emuliert Aspose.Words das Rendern von Metadateien auf seine Standardgröße in Pixeln.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist **true**.
## Siehe auch

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
