---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact Methode"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll in C++."
type: docs
weight: 17500
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Liest oder legt einen Wert fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Hinweise


Der Standardwert ist **false** und Absatzgrafiken (Unterstreichungen, Textbetonungen usw.) werden im logischen Aufbau des Dokuments als "Span" markiert.

Wenn der Wert **true** ist, werden die Absatzgrafiken als "Artifact" markiert.

Dieser Wert wird ignoriert, wenn [ExportDocumentStructure](../get_exportdocumentstructure/) **false** ist.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
