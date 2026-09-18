---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts Methode"
linktitle: "get_EmbedFullFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts Methode. Steuert, wie Schriftarten in die resultierenden PDF-Dokumente in C++ eingebettet werden."
type: docs
weight: 14000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Steuert, wie Schriftarten in die resultierenden PDF‑Dokumente eingebettet werden.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Hinweise


Der Standardwert ist **false**, was bedeutet, dass die Schriftarten vor dem Einbetten unterteilt werden. Das Unterteilen ist nützlich, wenn Sie die Dateigröße der Ausgabe kleiner halten möchten. Das Unterteilen entfernt alle nicht verwendeten Glyphen aus einer Schriftart.

Wenn dieser Wert auf **true** gesetzt wird, wird eine vollständige Schriftdatei ohne Unterteilung in das PDF eingebettet. Dies führt zu größeren Ausgabedateien, kann jedoch eine nützliche Option sein, wenn Sie das resultierende PDF später bearbeiten möchten (z. B. mehr Text hinzufügen).

Einige Schriftarten sind groß (mehrere Megabyte) und das Einbetten ohne Unterteilung führt zu großen Ausgabedokumenten.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
