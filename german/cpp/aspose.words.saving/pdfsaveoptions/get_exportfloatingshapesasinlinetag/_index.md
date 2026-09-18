---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag Methode"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob schwebende Formen als Inline‑Tags in der Dokumentstruktur in C++ exportiert werden."
type: docs
weight: 16500
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


Liest oder legt einen Wert fest, der bestimmt, ob schwebende Formen als Inline‑Tags in der Dokumentstruktur exportiert werden.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## Hinweise


Standardwert ist **false** und schwebende Formen werden als Block‑Tags exportiert, die nach dem Absatz, in dem sie verankert sind, platziert werden.

Wenn der Wert **true** ist, werden schwebende Formen als Inline‑Tags exportiert, die innerhalb des Absatzes, in dem sie verankert sind, platziert werden.

Dieser Wert wird ignoriert, wenn [ExportDocumentStructure](../get_exportdocumentstructure/) **false** ist.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
