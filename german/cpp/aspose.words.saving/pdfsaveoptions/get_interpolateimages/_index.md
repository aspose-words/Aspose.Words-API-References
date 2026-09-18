---
title: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages Methode"
linktitle: "get_InterpolateImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages Methode. Ein Flag, das angibt, ob Bildinterpolation von einem konformen Reader durchgeführt werden soll. Wenn **false** angegeben ist, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen das Standardverhalten des Readers verwendet, in C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


Ein Flag, das angibt, ob Bildinterpolation von einem konformen Reader durchgeführt werden soll. Wenn **false** angegeben wird, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen das Standardverhalten des Readers verwendet.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Hinweise


Wenn die Auflösung eines Quellbildes deutlich niedriger ist als die des Ausgabegeräts, deckt jede Quellprobe viele Geräte‑Pixel ab. Infolgedessen können Bilder gezackt oder blockig erscheinen. Diese visuellen Artefakte können durch Anwendung eines Bildinterpolations‑Algorithmus während des Renderns reduziert werden. Anstatt alle von einer Quellprobe abgedeckten Pixel mit derselben Farbe zu malen, versucht die Bildinterpolation einen sanften Übergang zwischen benachbarten Probenwerten zu erzeugen.

Ein konformer Reader kann wählen, diese PDF‑Funktion nicht zu implementieren, oder jede beliebige spezifische Implementierung der Interpolation zu verwenden, die er wünscht.

Der Standardwert ist **false**.

Das Interpolations‑Flag ist durch die PDF/A‑Konformität verboten. Der Wert **false** wird beim Speichern als PDF/A automatisch verwendet.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
