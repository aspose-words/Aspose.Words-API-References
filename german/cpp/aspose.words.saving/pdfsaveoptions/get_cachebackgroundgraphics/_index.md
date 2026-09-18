---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics Methode"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics Methode. Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Grafiken, die im Hintergrund des Dokuments platziert sind, im C++-Code zwischengespeichert werden sollen."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Liest oder legt einen Wert fest, der bestimmt, ob Grafiken, die im Hintergrund des Dokuments platziert werden, zwischengespeichert werden sollen oder nicht.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Hinweise


Standardwert ist **true** und Hintergrundgrafiken werden als xObject in das PDF-Dokument geschrieben.

Wenn der Wert **false** ist, werden Hintergrundgrafiken nicht zwischengespeichert.

Einige Formen werden für das Caching nicht unterstützt (Formen mit Feldern, Lesezeichen, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
