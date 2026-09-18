---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag Methode"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag Methode. Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob ein \\\"Span\\\"-Tag in der Dokumentstruktur erstellt wird, um die Textsprache in C++ zu exportieren."
type: docs
weight: 17000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Liest oder legt einen Wert fest, der bestimmt, ob ein \"Span\"-Tag in der Dokumentstruktur erstellt werden soll, um die Textsprache zu exportieren.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Hinweise


Standardwert ist **false** und das Attribut \"Lang\" wird einer markierten Inhaltssequenz in einem Seiteninhaltsstrom angehängt.

Wenn der Wert **true** ist, wird für den Text mit nicht‑Standard‑Sprache ein \"Span\"-Tag erstellt und das Attribut \"Lang\" wird diesem Tag angehängt.

Dieser Wert wird ignoriert, wenn [ExportDocumentStructure](../get_exportdocumentstructure/) **false** ist.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
